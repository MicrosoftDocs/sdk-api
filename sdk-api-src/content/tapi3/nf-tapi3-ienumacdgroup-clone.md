---
UID: NF:tapi3.IEnumACDGroup.Clone
title: IEnumACDGroup::Clone (tapi3.h)
description: The IEnumACDGroup::Clone method (tapi3.h) creates another enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumACDGroup interface","IEnumACDGroup interface [TAPI 2.2]","Clone method","IEnumACDGroup.Clone","IEnumACDGroup::Clone","_tapi3_ienumacdgroup_clone","tapi3.ienumacdgroup_clone","tapi3cc/IEnumACDGroup::Clone"]
old-location: tapi3\ienumacdgroup_clone.htm
tech.root: tapi3
ms.assetid: 202f8534-9990-4e69-b3b8-8a8884b651f1
ms.date: 08/09/2022
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumACDGroup interface, IEnumACDGroup interface [TAPI 2.2],Clone method, IEnumACDGroup.Clone, IEnumACDGroup::Clone, _tapi3_ienumacdgroup_clone, tapi3.ienumacdgroup_clone, tapi3cc/IEnumACDGroup::Clone
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumACDGroup::Clone
 - tapi3/IEnumACDGroup::Clone
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
 - IEnumACDGroup.Clone
---

# IEnumACDGroup::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a> interface.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a> interface returned by <b>IEnumACDGroup::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumACDGroup</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
