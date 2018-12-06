---
UID: NF:tapi3if.IEnumSubStream.Reset
title: IEnumSubStream::Reset
author: windows-sdk-content
description: The Reset method resets to the beginning of the enumeration sequence.
old-location: tapi3\ienumsubstream_reset.htm
tech.root: tapi
ms.assetid: 72b91c81-8cfa-4879-bfcf-87fde38fcc79
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumSubStream interface [TAPI 2.2],Reset method, IEnumSubStream.Reset, IEnumSubStream::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumSubStream interface, _tapi3_ienumsubstream_reset, tapi3.ienumsubstream_reset, tapi3if/IEnumSubStream::Reset
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - IEnumSubStream.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSubStream::Reset


## -description


The 
<b>Reset</b> method resets to the beginning of the enumeration sequence.


## -parameters






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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d9076a32-983e-48d4-b025-5fc770156df6">IEnumSubStream</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

