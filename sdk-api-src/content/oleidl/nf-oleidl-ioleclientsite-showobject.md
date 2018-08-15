---
UID: NF:oleidl.IOleClientSite.ShowObject
title: IOleClientSite::ShowObject
author: windows-sdk-content
description: Asks a container to display its object to the user. This method ensures that the container itself is visible and not minimized.
old-location: com\ioleclientsite_showobject.htm
old-project: com
ms.assetid: ba502a3d-2042-4978-a152-636a887c61fc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleClientSite interface [COM],ShowObject method, IOleClientSite.ShowObject, IOleClientSite::ShowObject, ShowObject, ShowObject method [COM], ShowObject method [COM],IOleClientSite interface, _ole_ioleclientsite_showobject, com.ioleclientsite_showobject, oleidl/IOleClientSite::ShowObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleClientSite.ShowObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

