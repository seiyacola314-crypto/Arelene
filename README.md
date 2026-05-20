# Arelene
import { GoogleGenAI } from "https://esm.run/@google/genai";
const ai = new GoogleGenAI({ apiKey: userKey });
const response = await ai.models.generateContent(
{ model: "gemini-2.5-flash-lite", // ← 절대 변경 금지
contents: history, // 멀티턴 누적
config: { systemInstruction: BTS_KNOWLEDGE } });
console.log(response.text);
