import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { UserCircle } from "lucide-react";

export default function CoralConnect() {
  return (
    <main className="p-6 max-w-5xl mx-auto">
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold text-teal-700 mb-2">Coral Connect</h1>
        <p className="text-lg text-gray-600">Un réseau social pour sauver les récifs coralliens 🌊</p>
      </header>

      <section className="grid md:grid-cols-3 gap-6 mb-10">
        <Card className="col-span-2">
          <CardContent className="p-4">
            <div className="flex items-center gap-3 mb-4">
              <UserCircle className="w-10 h-10 text-teal-500" />
              <Input placeholder="Qu’avez-vous observé aujourd’hui sur les coraux ?" />
            </div>
            <Textarea placeholder="Partagez votre expérience ou vos idées pour les protéger..." className="mb-4" />
            <Button className="bg-teal-600 hover:bg-teal-700">Publier</Button>
          </CardContent>
        </Card>

        <Card>
          <CardContent className="p-4">
            <h2 className="text-xl font-semibold mb-3">📊 Donnée du jour</h2>
            <p className="text-lg font-bold text-red-600">33% des récifs coralliens ont déjà disparu</p>
            <p className="text-sm text-gray-600 mt-2">Selon les rapports de l’ONU, cette perte est due au réchauffement climatique, à la pollution et à la surpêche.</p>
          </CardContent>
        </Card>
      </section>

      <section>
        <h2 className="text-2xl font-semibold mb-4">📸 Fil de publications</h2>
        <div className="grid gap-4">
          <Card>
            <CardContent className="p-4">
              <p><strong>@OcéanLover :</strong> J’ai vu des coraux blanchis à Bali... 😢 On doit agir vite !</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-4">
              <p><strong>@CoralGuard :</strong> Grâce aux aires marines protégées aux Philippines, les coraux revivent ! 🌱🐠</p>
            </CardContent>
          </Card>
        </div>
      </section>
    </main>
  );
}
