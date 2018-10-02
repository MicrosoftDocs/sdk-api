---
UID: NF:tapi3if.ITTAPI.Shutdown
title: ITTAPI::Shutdown
author: windows-sdk-content
description: The Shutdown method shuts down a TAPI session.
old-location: tapi3\ittapi_shutdown.htm
tech.root: TAPI
ms.assetid: 64abb427-d41a-4670-a01c-095c678de6ff
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITTAPI interface [TAPI 2.2],Shutdown method, ITTAPI.Shutdown, ITTAPI::Shutdown, Shutdown, Shutdown method [TAPI 2.2], Shutdown method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_shutdown, tapi3.ittapi_shutdown, tapi3if/ITTAPI::Shutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI::Shutdown


## -description


The 
<b>Shutdown</b> method shuts down a TAPI session.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
TAPI session has already been shut down.

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
</table>
 




## -remarks



One reason why 
<b>Shutdown</b> might fail is if 
<a href="https://msdn.microsoft.com/822ca3fe-8deb-4fe3-8b83-060eae69840c">Initialize</a> was not previously called successfully.




## -see-also




<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

