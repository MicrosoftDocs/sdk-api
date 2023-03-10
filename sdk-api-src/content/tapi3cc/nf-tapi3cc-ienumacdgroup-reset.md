---
UID: NF:tapi3cc.IEnumACDGroup.Reset
title: IEnumACDGroup::Reset (tapi3cc.h)
description: The IEnumACDGroup::Reset method (tapi3cc.h) resets the enumeration sequence to the beginning.
helpviewer_keywords: ["IEnumACDGroup interface [TAPI 2.2]","Reset method","IEnumACDGroup.Reset","IEnumACDGroup::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumACDGroup interface","_tapi3_ienumacdgroup_reset","tapi3.ienumacdgroup_reset","tapi3cc/IEnumACDGroup::Reset"]
old-location: tapi3\ienumacdgroup_reset.htm
tech.root: tapi3
ms.assetid: 66c51bdd-c820-4670-a80d-27cfa080f08f
ms.date: 08/09/2022
ms.keywords: IEnumACDGroup interface [TAPI 2.2],Reset method, IEnumACDGroup.Reset, IEnumACDGroup::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumACDGroup interface, _tapi3_ienumacdgroup_reset, tapi3.ienumacdgroup_reset, tapi3cc/IEnumACDGroup::Reset
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
 - IEnumACDGroup::Reset
 - tapi3cc/IEnumACDGroup::Reset
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
 - IEnumACDGroup.Reset
---

# IEnumACDGroup::Reset


## -description

The 
<b>Reset</b> method resets the enumeration sequence to the beginning.



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
