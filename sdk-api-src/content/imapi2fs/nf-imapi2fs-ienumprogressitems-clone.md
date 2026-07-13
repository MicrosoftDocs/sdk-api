---
UID: NF:imapi2fs.IEnumProgressItems.Clone
title: IEnumProgressItems::Clone (imapi2fs.h)
description: Creates another enumerator that contains the same enumeration state as the current one. (IEnumProgressItems.Clone)
helpviewer_keywords: ["Clone","Clone method [IMAPI]","Clone method [IMAPI]","IEnumProgressItems interface","IEnumProgressItems interface [IMAPI]","Clone method","IEnumProgressItems.Clone","IEnumProgressItems::Clone","imapi.ienumprogressitems_clone","imapi2fs/IEnumProgressItems::Clone"]
old-location: imapi\ienumprogressitems_clone.htm
tech.root: imapi
ms.assetid: 21167aaa-655d-48de-9f83-b98c8a91c482
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [IMAPI], Clone method [IMAPI],IEnumProgressItems interface, IEnumProgressItems interface [IMAPI],Clone method, IEnumProgressItems.Clone, IEnumProgressItems::Clone, imapi.ienumprogressitems_clone, imapi2fs/IEnumProgressItems::Clone
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
 - IEnumProgressItems::Clone
 - imapi2fs/IEnumProgressItems::Clone
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
 - IEnumProgressItems.Clone
---

# IEnumProgressItems::Clone


## -description

Creates another enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppEnum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnum</i> when done.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
</table>

## -remarks

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>
