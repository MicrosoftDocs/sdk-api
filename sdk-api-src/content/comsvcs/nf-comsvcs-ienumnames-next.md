---
UID: NF:comsvcs.IEnumNames.Next
title: IEnumNames::Next (comsvcs.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumNames.Next)
helpviewer_keywords: ["IEnumNames interface [COM+]","Next method","IEnumNames.Next","IEnumNames::Next","Next","Next method [COM+]","Next method [COM+]","IEnumNames interface","_cos_IEnumNames_Next","comsvcs/IEnumNames::Next","cos.ienumnames_next"]
old-location: cos\ienumnames_next.htm
tech.root: cos
ms.assetid: fa20453f-f170-442d-a927-6872ca75dbed
ms.date: 12/05/2018
ms.keywords: IEnumNames interface [COM+],Next method, IEnumNames.Next, IEnumNames::Next, Next, Next method [COM+], Next method [COM+],IEnumNames interface, _cos_IEnumNames_Next, comsvcs/IEnumNames::Next, cos.ienumnames_next
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
 - IEnumNames::Next
 - comsvcs/IEnumNames::Next
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
 - IEnumNames.Next
---

# IEnumNames::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of name values being requested.

### -param rgname [out]

An array in which the name values are to be returned and which must be of at least the size defined in the <i>celt</i> parameter.

### -param pceltFetched [out]

The number of elements returned in <i>rgname</i>, or <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
All elements requested were obtained successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements returned is less than the number specified in the <i>celt</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ienumnames">IEnumNames</a>
