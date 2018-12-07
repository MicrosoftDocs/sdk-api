---
UID: NF:rend.IEnumDirectory.Clone
title: IEnumDirectory::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienumdirectory_clone.htm
tech.root: tapi
ms.assetid: 64aaf773-842b-42cd-83b8-587ec1042382
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumDirectory interface, IEnumDirectory interface [TAPI 2.2],Clone method, IEnumDirectory.Clone, IEnumDirectory::Clone, _tapi3_ienumdirectory_clone, rend/IEnumDirectory::Clone, tapi3.ienumdirectory_clone
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
 - IEnumDirectory.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDirectory::Clone


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to the new 
<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a> object.


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
<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a> interface returned by <b>IEnumDirectory::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectory</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a>
 

 

