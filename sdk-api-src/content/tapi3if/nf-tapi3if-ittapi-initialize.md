---
UID: NF:tapi3if.ITTAPI.Initialize
title: ITTAPI::Initialize
author: windows-sdk-content
description: The Initialize method initializes TAPI. This method must be called before calling any other TAPI 3 method. The application must call the Shutdown method when ending a TAPI session.
old-location: tapi3\ittapi_initialize.htm
old-project: tapi
ms.assetid: 822ca3fe-8deb-4fe3-8b83-060eae69840c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITTAPI interface [TAPI 2.2],Initialize method, ITTAPI.Initialize, ITTAPI::Initialize, Initialize, Initialize method [TAPI 2.2], Initialize method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_initialize, tapi3.ittapi_initialize, tapi3if/ITTAPI::Initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.Initialize
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::Initialize


## -description


The 
<b>Initialize</b> method initializes TAPI. This method must be called before calling any other TAPI 3 method. The application must call the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method when ending a TAPI session.


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
TAPI has already been initialized.

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
 




## -see-also




<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

