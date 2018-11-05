---
UID: NF:oleidl.IOleObject.SetMoniker
title: IOleObject::SetMoniker
author: windows-sdk-content
description: Notifies an object of its container's moniker, the object's own moniker relative to the container, or the object's full moniker.
old-location: com\ioleobject_setmoniker.htm
tech.root: com
ms.assetid: 1313cd9a-757d-4716-abac-027cff9fee03
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IOleObject interface [COM],SetMoniker method, IOleObject.SetMoniker, IOleObject::SetMoniker, SetMoniker, SetMoniker method [COM], SetMoniker method [COM],IOleObject interface, _ole_ioleobject_setmoniker, com.ioleobject_setmoniker, oleidl/IOleObject::SetMoniker
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
 - IOleObject.SetMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleObject::SetMoniker


## -description


Notifies an object of its container's moniker, the object's own moniker relative to the container, or the object's full moniker.


## -parameters




### -param dwWhichMoniker [in]

The moniker is passed in <i>pmk</i>. Possible values are from the enumeration <a href="https://msdn.microsoft.com/3774c868-c312-4e7c-aa57-cdb13000a87c">OLEWHICHMK</a>.


### -param pmk [in]

Pointer to where to return the moniker.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 




## -remarks



A container that supports links to embedded objects must be able to inform an embedded object when its moniker has changed. Otherwise, subsequent attempts by link clients to bind to the object will fail. The <b>IOleObject::SetMoniker</b> method provides one way for a container to communicate this information.

The container can pass either its own moniker, an object's moniker relative to the container, or an object's full moniker. In practice, if a container passes anything other than an object's full moniker, each object calls the container back to request assignment of the full moniker, which the object requires to register itself in the running object table.

The moniker of an object relative to its container is stored by the object handler as part of the object's persistent state. The moniker of the object's container, however, must not be persistently stored inside the object because the container can be renamed at any time.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container calls <b>IOleObject::SetMoniker</b> when the container has been renamed, and the container's embedded objects currently or can potentially serve as link sources. Containers call SetMoniker mainly in the context of linking because an embedded object is already aware of its moniker. Even in the context of linking, calling this method is optional because objects can call <a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a> to force assignment of a new moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Upon receiving a call to <b>IOleObject::SetMoniker</b>, an object should register its full moniker in the running object table and send <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a> notification to all advise sinks that exist for the object.




## -see-also




<a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a>



<a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a>



<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a>
 

 

