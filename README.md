# js
export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Use POST" });
  const { text } = req.body || {};
  return res.json({ type: "text", text: `You said: ${text || ""}` });
}
