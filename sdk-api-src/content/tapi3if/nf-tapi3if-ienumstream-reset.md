---
UID: NF:tapi3if.IEnumStream.Reset
title: IEnumStream::Reset
author: windows-sdk-content
description: The Reset method resets to the beginning of the enumeration sequence.
old-location: tapi3\ienumstream_reset.htm
tech.root: Tapi
ms.assetid: 264b155c-4881-4170-bdc2-035b71d00f21
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IEnumStream interface [TAPI 2.2],Reset method, IEnumStream.Reset, IEnumStream::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumStream interface, _tapi3_ienumstream_reset, tapi3.ienumstream_reset, tapi3if/IEnumStream::Reset
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
 - IEnumStream.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumStream::Reset


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




<a href="https://msdn.microsoft.com/52e8c040-8bc5-4c9c-a697-ec05164adea2">IEnumStream</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

