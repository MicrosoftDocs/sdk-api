---
UID: NF:tapi3if.IEnumStream.Skip
title: IEnumStream::Skip (tapi3if.h)
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumstream_skip.htm
tech.root: Tapi
ms.assetid: aa9f3a77-4e5c-43b7-9526-b621a300c2ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumStream interface [TAPI 2.2],Skip method, IEnumStream.Skip, IEnumStream::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumStream interface, _tapi3_ienumstream_skip, tapi3.ienumstream_skip, tapi3if/IEnumStream::Skip
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
 - IEnumStream.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumStream::Skip


## -description


The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

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
 

 

