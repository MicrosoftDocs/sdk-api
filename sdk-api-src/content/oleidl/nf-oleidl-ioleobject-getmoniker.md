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

# IOleObject::GetMoniker


## -description


Retrieves an embedded object's moniker, which the caller can use to link to the object.


## -parameters




### -param dwAssign [in]

Determines how the moniker is assigned to the object. Depending on the value of <i>dwAssign</i>, <b>IOleObject::GetMoniker</b> does one of the following:

<ul>
<li>Obtains a moniker only if one has already been assigned.</li>
<li>Forces assignment of a moniker, if necessary, in order to satisfy the call.</li>
<li>Obtains a temporary moniker.</li>
</ul>

Values for <i>dwAssign</i> are specified in the enumeration <a href="https://msdn.microsoft.com/b69e3213-08c4-45f8-b1b3-4ca78e966251">OLEGETMONIKER</a>.

<div class="alert"><b>Note</b>   You cannot pass <a href="https://msdn.microsoft.com/b69e3213-08c4-45f8-b1b3-4ca78e966251">OLEGETMONIKER</a>_UNASSIGN when calling <b>IOleObject::GetMoniker</b>. This value is valid only when calling <b>IOleObject::GetMoniker</b>.</div>
<div> </div>

### -param dwWhichMoniker [in]

Specifies the form of the moniker being requested. Possible values are taken from the enumeration <a href="https://msdn.microsoft.com/3774c868-c312-4e7c-aa57-cdb13000a87c">OLEWHICHMK</a>.


### -param ppmk [out]

Address of <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> pointer variable that receives the interface pointer to the object's moniker. If an error occurs, <i>ppmk</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetMoniker</b>, it must increase the reference count on <i>ppmk</i>. It is the caller's responsibility to call Release when it is done with <i>ppmk</i>.


## -returns



This method returns S_OK on success.




## -remarks



The <b>IOleObject::GetMoniker</b> method returns an object's moniker. Like <a href="https://msdn.microsoft.com/1313cd9a-757d-4716-abac-027cff9fee03">IOleObject::SetMoniker</a>, this method is important only in the context of managing links to embedded objects and even in that case is optional. A potential link client that requires an object's moniker to bind to the object can call this method to obtain that moniker. The default implementation of <b>IOleObject::GetMoniker</b> calls the <a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a>, returning E_UNEXPECTED if the object is not running or does not have a valid pointer to a client site.




## -see-also




<a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a>



<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/1313cd9a-757d-4716-abac-027cff9fee03">IOleObject::SetMoniker</a>



<a href="https://msdn.microsoft.com/b69e3213-08c4-45f8-b1b3-4ca78e966251">OLEGETMONIKER</a>



<a href="https://msdn.microsoft.com/3774c868-c312-4e7c-aa57-cdb13000a87c">OLEWHICHMK</a>
 

 

