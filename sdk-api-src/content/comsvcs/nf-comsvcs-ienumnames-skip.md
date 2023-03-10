---
UID: NF:comsvcs.IEnumNames.Skip
title: IEnumNames::Skip (comsvcs.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumNames.Skip)
helpviewer_keywords: ["IEnumNames interface [COM+]","Skip method","IEnumNames.Skip","IEnumNames::Skip","Skip","Skip method [COM+]","Skip method [COM+]","IEnumNames interface","_cos_IEnumNames_Skip","comsvcs/IEnumNames::Skip","cos.ienumnames_skip"]
old-location: cos\ienumnames_skip.htm
tech.root: cos
ms.assetid: e45da100-688a-421e-a8cd-19fede5aac83
ms.date: 12/05/2018
ms.keywords: IEnumNames interface [COM+],Skip method, IEnumNames.Skip, IEnumNames::Skip, Skip, Skip method [COM+], Skip method [COM+],IEnumNames interface, _cos_IEnumNames_Skip, comsvcs/IEnumNames::Skip, cos.ienumnames_skip
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
 - IEnumNames::Skip
 - comsvcs/IEnumNames::Skip
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
 - IEnumNames.Skip
---

# IEnumNames::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of elements to be skipped.

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
The requested number of elements was skipped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements skipped was not the same as the number requested.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a>
