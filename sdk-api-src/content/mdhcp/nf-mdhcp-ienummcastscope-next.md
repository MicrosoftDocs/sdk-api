---
UID: NF:mdhcp.IEnumMcastScope.Next
title: IEnumMcastScope::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienummcastscope_next.htm
tech.root: TAPI
ms.assetid: f7618414-c2fc-46c8-8f9d-c1ad217c8d94
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumMcastScope interface [TAPI 2.2],Next method, IEnumMcastScope.Next, IEnumMcastScope::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumMcastScope interface, _tapi3_ienummcastscope_next, mdhcp/IEnumMcastScope::Next, tapi3.ienummcastscope_next
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
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IEnumMcastScope.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumMcastScope::Next


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppScopes [out]

Pointer to the 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> interface.


### -param pceltFetched [out]

Pointer to the number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppScopes</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> interface returned by <b>IEnumMcastScope::Next</b>. The application must call <b>Release</b> on the 
<b>IMcastScope</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a>
 

 

