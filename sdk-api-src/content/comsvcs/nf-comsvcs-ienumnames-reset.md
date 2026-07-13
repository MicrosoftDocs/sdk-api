---
UID: NF:comsvcs.IEnumNames.Reset
title: IEnumNames::Reset (comsvcs.h)
description: Resets the enumeration sequence to the beginning. (IEnumNames.Reset)
helpviewer_keywords: ["IEnumNames interface [COM+]","Reset method","IEnumNames.Reset","IEnumNames::Reset","Reset","Reset method [COM+]","Reset method [COM+]","IEnumNames interface","_cos_IEnumNames_Reset","comsvcs/IEnumNames::Reset","cos.ienumnames_reset"]
old-location: cos\ienumnames_reset.htm
tech.root: cos
ms.assetid: e7b7e703-f5d5-430f-8fa6-c26a236eab88
ms.date: 12/05/2018
ms.keywords: IEnumNames interface [COM+],Reset method, IEnumNames.Reset, IEnumNames::Reset, Reset, Reset method [COM+], Reset method [COM+],IEnumNames interface, _cos_IEnumNames_Reset, comsvcs/IEnumNames::Reset, cos.ienumnames_reset
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumNames::Reset
 - comsvcs/IEnumNames::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IEnumNames.Reset
---

# IEnumNames::Reset


## -description

Resets the enumeration sequence to the beginning.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The enumeration sequence was reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The enumeration sequence was reset, but there are no items in the enumerator.

</td>
</tr>
</table>

## -remarks

You can use the S_FALSE return value as an optimization to detect an empty enumeration.

A call to this method, resetting the sequence, does not guarantee that the same set of objects will be enumerated after the reset, because the collection may have changed.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a>
