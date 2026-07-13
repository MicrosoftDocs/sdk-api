---
UID: NF:tapi3if.IEnumPhone.Skip
title: IEnumPhone::Skip (tapi3if.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumPhone.Skip)
helpviewer_keywords: ["IEnumPhone interface [TAPI 2.2]","Skip method","IEnumPhone.Skip","IEnumPhone::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumPhone interface","_tapi3_ienumphone_skip","tapi3.ienumphone_skip","tapi3if/IEnumPhone::Skip"]
old-location: tapi3\ienumphone_skip.htm
tech.root: tapi3
ms.assetid: fe137da2-2c12-4732-9ab8-adf07381c692
ms.date: 12/05/2018
ms.keywords: IEnumPhone interface [TAPI 2.2],Skip method, IEnumPhone.Skip, IEnumPhone::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumPhone interface, _tapi3_ienumphone_skip, tapi3.ienumphone_skip, tapi3if/IEnumPhone::Skip
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumPhone::Skip
 - tapi3if/IEnumPhone::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumPhone.Skip
---

# IEnumPhone::Skip


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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a>
