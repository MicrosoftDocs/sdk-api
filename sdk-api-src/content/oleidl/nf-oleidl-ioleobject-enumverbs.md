---
UID: NF:oleidl.IOleObject.EnumVerbs
title: IOleObject::EnumVerbs
author: windows-sdk-content
description: Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.
old-location: com\ioleobject_enumverbs.htm
tech.root: com
ms.assetid: c67770d0-e478-41dc-9028-1e0a6cb9e3c7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumVerbs, EnumVerbs method [COM], EnumVerbs method [COM],IOleObject interface, IOleObject interface [COM],EnumVerbs method, IOleObject.EnumVerbs, IOleObject::EnumVerbs, _ole_ioleobject_enumverbs, com.ioleobject_enumverbs, oleidl/IOleObject::EnumVerbs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.EnumVerbs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

