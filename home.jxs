"use client";
import { useState } from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";

export default function LessonIntroTransistor() {
  const [type, setType] = useState("NPN");

  const transistorData = {
    NPN: {
      color: "from-blue-500 to-cyan-400",
      emitter: "Medium size, heavily doped (releases electrons)",
      base: "Very thin, lightly doped (controls current flow)",
      collector: "Large, moderately doped (collects electrons)",
      direction: "Upwards (Emitter → Collector)",
      description:
        "An NPN transistor consists of two N-type regions separated by a thin P-type base. When a small current enters the base, it allows a much larger current to flow from collector to emitter.",
    },
    PNP: {
      color: "from-pink-500 to-rose-400",
      emitter: "Medium size, heavily doped (releases holes)",
      base: "Very thin, lightly doped (controls hole flow)",
      collector: "Large, moderately doped (collects holes)",
      direction: "Downwards (Emitter → Collector)",
      description:
        "A PNP transistor consists of two P-type regions separated by a thin N-type base. Current flows in the opposite direction to NPN, using holes instead of electrons.",
    },
  };

  const info = transistorData[type];

  return (
    <div className="min-h-screen bg-gradient-to-b from-slate-900 to-slate-800 text-white flex flex-col items-center py-10 px-6">
      <h1 className="text-4xl font-bold mb-6 text-center">
        Lesson 2: Introduction to Transistors
      </h1>

      <div className="flex gap-4 mb-8">
        <Button
          onClick={() => setType("NPN")}
          variant={type === "NPN" ? "default" : "outline"}
        >
          NPN
        </Button>
        <Button
          onClick={() => setType("PNP")}
          variant={type === "PNP" ? "default" : "outline"}
        >
          PNP
        </Button>
      </div>

      <Card className="w-full max-w-3xl bg-slate-800/50 backdrop-blur-xl border border-slate-700 rounded-2xl shadow-xl">
        <CardContent className="p-8 flex flex-col md:flex-row items-center justify-between gap-8">
          {/* Transistor Visual */}
          <div className="relative w-64 h-64">
            <motion.div
              className={`absolute inset-0 rounded-full bg-gradient-to-br ${info.color} opacity-20`}
              layout
              transition={{ duration: 0.5 }}
            />
            <div className="absolute inset-0 flex flex-col items-center justify-between">
              {/* Collector */}
              <div className="text-center group">
                <div className="w-6 h-6 bg-white rounded-full mx-auto mb-1" />
                <p className="text-sm font-semibold">Collector</p>
                <span className="opacity-0 group-hover:opacity-100 text-xs text-gray-300">
                  {info.collector}
                </span>
              </div>

              {/* Arrow showing direction */}
              <motion.div
                className="flex flex-col items-center justify-center"
                animate={{ rotate: type === "NPN" ? 0 : 180 }}
                transition={{ duration: 0.6 }}
              >
                <motion.div
                  animate={{
                    y: [0, -20, 0],
                  }}
                  transition={{
                    repeat: Infinity,
                    duration: 2,
                    ease: "easeInOut",
                  }}
                  className="w-2 h-24 bg-gradient-to-b from-yellow-300 to-yellow-600 rounded-full"
                />
                <motion.div
                  className="w-0 h-0 border-l-8 border-r-8 border-t-[12px] border-t-yellow-400"
                />
              </motion.div>

              {/* Emitter */}
              <div className="text-center group">
                <div className="w-6 h-6 bg-white rounded-full mx-auto mb-1" />
                <p className="text-sm font-semibold">Emitter</p>
                <span className="opacity-0 group-hover:opacity-100 text-xs text-gray-300">
                  {info.emitter}
                </span>
              </div>
            </div>

            {/* Base */}
            <div className="absolute left-1/2 top-1/2 -translate-x-1/2">
              <div className="flex flex-col items-center group">
                <div className="w-6 h-6 bg-white rounded-full mb-1" />
                <p className="text-sm font-semibold">Base</p>
                <span className="opacity-0 group-hover:opacity-100 text-xs text-gray-300">
                  {info.base}
                </span>
              </div>
            </div>
          </div>

          {/* Text Section */}
          <div className="max-w-md">
            <h2 className="text-2xl font-bold mb-2">{type} Transistor</h2>
            <p className="text-gray-300 mb-4">{info.description}</p>
            <ul className="space-y-2 text-gray-400 text-sm list-disc list-inside">
              <li>
                <strong>Emitter (E):</strong> {info.emitter}
              </li>
              <li>
                <strong>Base (B):</strong> {info.base}
              </li>
              <li>
                <strong>Collector (C):</strong> {info.collector}
              </li>
            </ul>
          </div>
        </CardContent>
      </Card>

      <div className="mt-10 text-gray-400 max-w-2xl text-center">
        <p>
          The transistor acts as a bridge between analog and digital electronics.
          By controlling a small current at the base, it regulates a much larger
          current between collector and emitter — the core idea behind amplification
          and switching.
        </p>
      </div>
    </div>
  );
}
