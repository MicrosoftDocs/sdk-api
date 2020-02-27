---
UID: NF:tapi3.IEnumAgent.Skip
title: IEnumAgent::Skip (tapi3.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumagent_skip.htm
tech.root: Tapi
ms.assetid: 972e02f5-2aaf-4c9f-ab66-61d500b6f8ae
ms.date: 12/05/2018
ms.keywords: IEnumAgent interface [TAPI 2.2],Skip method, IEnumAgent.Skip, IEnumAgent::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumAgent interface, _tapi3_ienumagent_skip, tapi3.ienumagent_skip, tapi3cc/IEnumAgent::Skip
f1_keywords:
- tapi3/IEnumAgent.Skip
dev_langs:
- c++
req.header: tapi3.h
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
- IEnumAgent.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAgent::Skip


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
 

 

