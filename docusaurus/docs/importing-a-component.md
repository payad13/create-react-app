 import React, { useState } from "react";

export default function Kogapost() { const [showTaxiContact, setShowTaxiContact] = useState(false); const [showBusContact, setShowBusContact] = useState(false);

return ( <div className="bg-white min-h-screen p-6"> <h1 className="text-3xl font-bold mb-6">Kogapost</h1> <div className="grid grid-cols-2 gap-8"> {/* Taxi List */} <div> <h2 className="text-xl font-semibold mb-4">Taxi</h2> <div className="border rounded-2xl p-4 shadow-md"> <h3 className="text-lg font-medium mb-2 cursor-pointer text-blue-600 hover:underline" onClick={() => setShowTaxiContact(!showTaxiContact)} > Kalar - Slemani </h3> {showTaxiContact && ( <ul className="list-disc list-inside"> <li>Driver 1 - +964 770 000 0001</li> <li>Driver 2 - +964 770 000 0002</li> <li>Driver 3 - +964 770 000 0003</li> </ul> )} </div> </div>

{/* Bus List */}
    <div>
      <h2 className="text-xl font-semibold mb-4">Bus</h2>
      <div className="border rounded-2xl p-4 shadow-md">
        <h3
          className="text-lg font-medium mb-2 cursor-pointer text-blue-600 hover:underline"
          onClick={() => setShowBusContact(!showBusContact)}
        >
          Kalar - Slemani
        </h3>
        {showBusContact && (
          <ul className="list-disc list-inside">
            <li>Bus 1 - +964 750 000 0001</li>
            <li>Bus 2 - +964 750 000 0002</li>
            <li>Bus 3 - +964 750 000 0003</li>
          </ul>
        )}
      </div>
    </div>
  </div>
</div>

); }

