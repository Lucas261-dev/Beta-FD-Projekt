# Beta-FD-Projekt
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Label } from "@/components/ui/label";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
import { Textarea } from "@/components/ui/textarea";

export default function AdminDashboard() {
  return (
    <div className="p-4 space-y-6">
      <h1 className="text-2xl font-bold">Admin-Dashboard</h1>

      <Tabs defaultValue="einsatz" className="w-full">
        <TabsList>
          <TabsTrigger value="einsatz">Einsätze</TabsTrigger>
          <TabsTrigger value="personen">Personen</TabsTrigger>
          <TabsTrigger value="fahrzeuge">Fahrzeuge</TabsTrigger>
          <TabsTrigger value="protokolle">Protokolle</TabsTrigger>
          <TabsTrigger value="rollen">Rollenverwaltung</TabsTrigger>
        </TabsList>

        <TabsContent value="einsatz">
          <Card>
            <CardContent className="space-y-4 p-4">
              <Label>Einsatzbeschreibung</Label>
              <Textarea placeholder="Einsatzdetails hier eintragen..." />
              <Button>Speichern</Button>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="personen">
          <Card>
            <CardContent className="space-y-4 p-4">
              <Label>Person hinzufügen</Label>
              <Input placeholder="Vorname Nachname" />
              <Input placeholder="Geburtsdatum" />
              <Input placeholder="Rolle (z.B. Polizei, Zivilist)" />
              <Button>Speichern</Button>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="fahrzeuge">
          <Card>
            <CardContent className="space-y-4 p-4">
              <Label>Fahrzeugdaten</Label>
              <Input placeholder="Kennzeichen" />
              <Input placeholder="Fahrzeugtyp" />
              <Button>Speichern</Button>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="protokolle">
          <Card>
            <CardContent className="space-y-4 p-4">
              <Label>Neues Protokoll</Label>
              <Textarea placeholder="Protokolltext..." />
              <Button>Exportieren als Google Docs</Button>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="rollen">
          <Card>
            <CardContent className="space-y-4 p-4">
              <Label>Rolle erstellen / bearbeiten</Label>
              <Input placeholder="Rollenname (z.B. Admin, Dispatcher)" />
              <Button>Erstellen</Button>
            </CardContent>
          </Card>
        </TabsContent>
      </Tabs>
    </div>
  );
}
