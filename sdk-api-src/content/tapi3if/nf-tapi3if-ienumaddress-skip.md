---
UID: NF:tapi3if.IEnumAddress.Skip
title: IEnumAddress::Skip (tapi3if.h)
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumaddress_skip.htm
tech.root: Tapi
ms.assetid: 9e7aba07-940d-400a-8618-44aca6df2291
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumAddress interface [TAPI 2.2],Skip method, IEnumAddress.Skip, IEnumAddress::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumAddress interface, _tapi3_ienumaddress_skip, tapi3.ienumaddress_skip, tapi3if/IEnumAddress::Skip
ms.topic: method
f1_keywords: 
 - "tapi3if/IEnumAddress.Skip"
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
 - IEnumAddress.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAddress::Skip


## -description


The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>
 

 

