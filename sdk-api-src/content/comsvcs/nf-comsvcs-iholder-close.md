---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IHolder::Close


## -description


Closes the Holder.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This closes a Resource Dispenser's Holder, after which the Resource Dispenser probably released.

Before closing, any remaining inventory is destroyed by calling back to the Resource Dispenser's <a href="https://msdn.microsoft.com/94e3e340-7dde-4b7f-82a9-83cd2400bde5">IDispenserDriver::DestroyResource</a> method.



The following sequence describes how to close down a Resource Dispenser:

<ol>
<li>Obtain a reference to the Resource Dispenser (the object that exposes <a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>).
</li>
<li>Call a method in Resource Dispenser whose implementation calls <b>IHolder::Close</b>.
</li>
<li><b>IHolder::Close</b> destroys any remaining inventory by calling back to Resource Dispenser's <a href="https://msdn.microsoft.com/94e3e340-7dde-4b7f-82a9-83cd2400bde5">IDispenserDriver::DestroyResource</a> method.
</li>
<li><b>IHolder::Close</b> calls the Dispenser Manager to remove this Holder from the Holder list. (If no Holders remain, the Dispenser Manager object deletes itself.)
</li>
<li><b>IHolder::Close</b> releases its reference to Resource Dispenser's <a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a> interface. This is the reason you need a reference in step 1; otherwise, the Resource Dispenser would delete itself prematurely before the subsequent steps can be completed.
</li>
<li><b>IHolder::Close</b> returns to the Resource Dispenser.
</li>
<li>The Resource Dispenser calls <a href="https://msdn.microsoft.com/94e3e340-7dde-4b7f-82a9-83cd2400bde5">IDispenserDriver::DestroyResource</a>. The Holder now deletes itself.
</li>
<li>The method called in step 2 now returns.
</li>
<li>Release your final reference to the Resource Dispenser, which now deletes itself.
</li>
</ol>
Note that the <a href="https://msdn.microsoft.com/18633c7f-d589-4e38-82e7-7cdae3fbf1ba">IDispenserManager::RegisterDispenser</a> method does not call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on its <i>pDispenserDriver</i> object, but <b>IHolder::Close</b> does perform a <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on <i>pDispenserDriver</i>. This can cause the Resource Dispenser object to be destroyed prematurely. To prevent this premature destruction, the caller of <b>IHolder::Close</b> must hold a reference to the Resource Dispenser object as described in steps 1 and 5.





## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

