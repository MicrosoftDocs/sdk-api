---
UID: NF:tapi3if.IEnumSubStream.Next
title: IEnumSubStream::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumsubstream_next.htm
tech.root: TAPI
ms.assetid: fa8c4017-09ac-44e9-a7fa-922d0588d92a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumSubStream interface [TAPI 2.2],Next method, IEnumSubStream.Next, IEnumSubStream::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumSubStream interface, _tapi3_ienumsubstream_next, tapi3.ienumsubstream_next, tapi3if/IEnumSubStream::Next
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
 - IEnumSubStream.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSubStream::Next


## -description


The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> pointers returned.


### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


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
The <i>ppElements</i> parameter is not a valid pointer.

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



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface returned by <b>IEnumSubStream::Next</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>ITSubStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/d9076a32-983e-48d4-b025-5fc770156df6">IEnumSubStream</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

