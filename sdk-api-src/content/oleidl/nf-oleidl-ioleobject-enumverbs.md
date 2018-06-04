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

# IOleObject::EnumVerbs


## -description


Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.


## -parameters




### -param ppEnumOleVerb [out]

Address of <a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a> pointer variable that receives the interface pointer to the new enumerator object. Each time an object receives a call to <b>IOleObject::EnumVerbs</b>, it must increase the reference count on <i>ppEnumOleVerb</i>. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when it is done with <i>ppEnumOleVerb</i>. If an error occurs, <i>ppEnumOleVerb</i> must be set to <b>NULL</b>.


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
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Delegate to the default handler to use the entries in the registry to provide the enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_E_NOVERBS</b></dt>
</dl>
</td>
<td width="60%">
Object does not support any verbs.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a>



<a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>
 

 

