import { useState } from "react";
title: "Zručnosti",
content: `• Pokročilá znalosť MS Office (Word, Excel, PowerPoint).\n• Základy práce s AI nástrojmi.\n• Analytické myslenie, dôslednosť, organizovanosť.`,
},
"zaujmy": {
title: "Záujmy a vlastnosti",
content: `Rada čítam knihy autoriek ako Francine Riversová, Clarissa Pinkola Estés či Tessa Afsharová.\nZaujímam sa o interiérový dizajn, tvorbu dekorácií a prácu v záhrade.\nVo voľnom čase trávim čas s rodinou – turistika, opekanie, hry s deťmi.\n\nV práci sa vyznačujem zodpovednosťou, dôslednosťou a nasadením pre dosiahnutie cieľa.`,
},
"kontakt": {
title: "Kontakt",
content: `📞 0944 598 061\n✉️ stolarikova.dasa@gmail.com\n📍 Dolná Tižina 5/5, 013 04\n\nVodičský preukaz: skupina B (aktívny vodič)`,
},
};


return (
<div className="min-h-screen bg-gray-50 text-gray-800 flex flex-col items-center py-10 px-4">
<motion.h1
initial={{ opacity: 0, y: -20 }}
animate={{ opacity: 1, y: 0 }}
transition={{ duration: 0.6 }}
className="text-4xl font-bold mb-6 text-center"
>
Ing. Daša Stoláriková
</motion.h1>
<motion.p
initial={{ opacity: 0 }}
animate={{ opacity: 1 }}
transition={{ delay: 0.3 }}
className="text-lg text-gray-600 mb-8 text-center max-w-2xl"
>
Profesionálny životopis / Moderné portfólio
</motion.p>


<div className="flex flex-wrap justify-center gap-3 mb-8">
{Object.keys(sections).map((key) => (
<Button
key={key}
variant={active === key ? "default" : "outline"}
onClick={() => setActive(key)}
className="capitalize"
>
{sections[key].title}
</Button>
))}
</div>


<motion.div
key={active}
initial={{ opacity: 0, y: 20 }}
animate={{ opacity: 1, y: 0 }}
transition={{ duration: 0.4 }}
className="w-full max-w-3xl"
>
<Card className="shadow-md">
<CardContent className="p-6 whitespace-pre-line text-lg">
<h2 className="text-2xl font-semibold mb-4">{sections[active].title}</h2>
<p>{sections[active].content}</p>
</CardContent>
</Card>
</motion.div>
</div>
);
}
