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

# IOleClientSite::ShowObject


## -description


Asks a container to display its object to the user. This method ensures that the container itself is visible and not minimized.


## -parameters






## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Client site is in an OLE 1 container.

</td>
</tr>
</table>
 




## -remarks



After a link client binds to a link source, it commonly calls <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> on the link source, usually requesting the source to perform some action requiring that it display itself to the user. As part of its implementation of <b>IOleObject::DoVerb</b>, the link source can call <b>ShowObject</b>, which forces the client to show the link source as best it can. If the link source's container is itself an embedded object, it will recursively invoke <b>ShowObject</b> on its own container.

Having called the <b>ShowObject</b> method, a link source has no guarantee of being appropriately displayed because its container may not be able to do so at the time of the call. The <b>ShowObject</b> method does not guarantee visibility, only that the container will do the best it can.




## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a>
 

 

