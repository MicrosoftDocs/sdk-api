---
UID: NF:tapi3cc.IEnumACDGroup.Skip
title: IEnumACDGroup::Skip (tapi3cc.h)
description: The IEnumACDGroup::Skip method (tapi3cc.h) skips over the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumACDGroup interface [TAPI 2.2]","Skip method","IEnumACDGroup.Skip","IEnumACDGroup::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumACDGroup interface","_tapi3_ienumacdgroup_skip","tapi3.ienumacdgroup_skip","tapi3cc/IEnumACDGroup::Skip"]
old-location: tapi3\ienumacdgroup_skip.htm
tech.root: tapi3
ms.assetid: 58f794cc-da10-4772-9afe-078337b7734b
ms.date: 08/09/2022
ms.keywords: IEnumACDGroup interface [TAPI 2.2],Skip method, IEnumACDGroup.Skip, IEnumACDGroup::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumACDGroup interface, _tapi3_ienumacdgroup_skip, tapi3.ienumacdgroup_skip, tapi3cc/IEnumACDGroup::Skip
req.header: tapi3cc.h
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
 - IEnumACDGroup::Skip
 - tapi3cc/IEnumACDGroup::Skip
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
 - IEnumACDGroup.Skip
---

# IEnumACDGroup::Skip


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

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
