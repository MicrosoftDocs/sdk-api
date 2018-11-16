---
UID: NF:rend.IEnumDirectoryObject.Clone
title: IEnumDirectoryObject::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumdirectoryobject_clone.htm
tech.root: Tapi
ms.assetid: 2be8430e-2968-416f-9503-b77d6abd6a12
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumDirectoryObject interface, IEnumDirectoryObject interface [TAPI 2.2],Clone method, IEnumDirectoryObject.Clone, IEnumDirectoryObject::Clone, _tapi3_ienumdirectoryobject_clone, rend/IEnumDirectoryObject::Clone, tapi3.ienumdirectoryobject_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - IEnumDirectoryObject.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rend.h
: 
- IEnumDirectoryObject.Clone
: 
---

# IEnumDirectoryObject::Clone


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to the new 
<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a> object.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a> interface returned by <b>IEnumDirectoryObject::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectoryObject</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a>
 

 

