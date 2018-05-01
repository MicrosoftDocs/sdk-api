---
UID: NF:mdhcp.IEnumMcastScope.Clone
title: IEnumMcastScope::Clone method
author: windows-driver-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: tapi3\ienummcastscope_clone.htm
old-project: Tapi
ms.assetid: 96b2a09f-8a02-471d-a738-f81a8132e0c1
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: Clone method [TAPI 2.2], Clone method [TAPI 2.2], IEnumMcastScope interface, Clone,IEnumMcastScope.Clone, IEnumMcastScope, IEnumMcastScope interface [TAPI 2.2], Clone method, IEnumMcastScope::Clone, _tapi3_ienummcastscope_clone, mdhcp/IEnumMcastScope::Clone, tapi3.ienummcastscope_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mdhcp.dll
api_name:
-	IEnumMcastScope.Clone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumMcastScope::Clone method


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to the new 
<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a> object.


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
<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a> interface returned by <b>IEnumMcastScope::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumMcastScope</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a>
 

 

