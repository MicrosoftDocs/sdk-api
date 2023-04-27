---
UID: NF:tapi3cc.IEnumACDGroup.Next
title: IEnumACDGroup::Next (tapi3cc.h)
description: The IEnumACDGroup::Next method (tapi3cc.h) gets the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumACDGroup interface [TAPI 2.2]","Next method","IEnumACDGroup.Next","IEnumACDGroup::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumACDGroup interface","_tapi3_ienumacdgroup_next","tapi3.ienumacdgroup_next","tapi3cc/IEnumACDGroup::Next"]
old-location: tapi3\ienumacdgroup_next.htm
tech.root: tapi3
ms.assetid: 20cad3aa-2c8c-4ef8-bb3a-b7662b125475
ms.date: 08/09/2022
ms.keywords: IEnumACDGroup interface [TAPI 2.2],Next method, IEnumACDGroup.Next, IEnumACDGroup::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumACDGroup interface, _tapi3_ienumacdgroup_next, tapi3.ienumacdgroup_next, tapi3cc/IEnumACDGroup::Next
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
 - IEnumACDGroup::Next
 - tapi3cc/IEnumACDGroup::Next
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
 - IEnumACDGroup.Next
---

# IEnumACDGroup::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> list of pointers returned.

### -param pceltFetched [in, out]

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface returned by <b>IEnumACDGroup::Next</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
