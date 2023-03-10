---
UID: NF:imapi2fs.IEnumProgressItems.Next
title: IEnumProgressItems::Next (imapi2fs.h)
description: Retrieves a specified number of items in the enumeration sequence. (IEnumProgressItems.Next)
helpviewer_keywords: ["IEnumProgressItems interface [IMAPI]","Next method","IEnumProgressItems.Next","IEnumProgressItems::Next","Next","Next method [IMAPI]","Next method [IMAPI]","IEnumProgressItems interface","imapi.ienumprogressitems_next","imapi2fs/IEnumProgressItems::Next"]
old-location: imapi\ienumprogressitems_next.htm
tech.root: imapi
ms.assetid: 9a6b4838-921b-444d-8ac2-f26d9762d9ce
ms.date: 12/05/2018
ms.keywords: IEnumProgressItems interface [IMAPI],Next method, IEnumProgressItems.Next, IEnumProgressItems::Next, Next, Next method [IMAPI], Next method [IMAPI],IEnumProgressItems interface, imapi.ienumprogressitems_next, imapi2fs/IEnumProgressItems::Next
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IEnumProgressItems::Next
 - imapi2fs/IEnumProgressItems::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IEnumProgressItems.Next
---

# IEnumProgressItems::Next


## -description

Retrieves a specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

Number of items to retrieve.

### -param rgelt [out]

Array of <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a> interfaces. You must release each interface in rgelt when done.

### -param pceltFetched [out]

Number of elements returned in rgelt. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one. Otherwise, initialize the value of <i>pceltFetched</i> to 0 before calling this method.

## -returns

S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>

## -remarks

If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/imapi/ienumprogressitems-remotenext">IEnumProgressItems::RemoteNext</a>
