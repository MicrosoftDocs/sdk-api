---
UID: NF:imapi2fs.IProgressItems.get_EnumProgressItems
title: IProgressItems::get_EnumProgressItems (imapi2fs.h)
description: Retrieves the list of progress items from the collection. (IProgressItems.get_EnumProgressItems)
helpviewer_keywords: ["IProgressItems interface [IMAPI]","get_EnumProgressItems method","IProgressItems.get_EnumProgressItems","IProgressItems::get_EnumProgressItems","get_EnumProgressItems","get_EnumProgressItems method [IMAPI]","get_EnumProgressItems method [IMAPI]","IProgressItems interface","imapi.iprogressitems_get_enumprogressitems","imapi2fs/IProgressItems::get_EnumProgressItems"]
old-location: imapi\iprogressitems_get_enumprogressitems.htm
tech.root: imapi
ms.assetid: 746b05b7-ddba-458c-bc9b-4913da5fa8b5
ms.date: 12/05/2018
ms.keywords: IProgressItems interface [IMAPI],get_EnumProgressItems method, IProgressItems.get_EnumProgressItems, IProgressItems::get_EnumProgressItems, get_EnumProgressItems, get_EnumProgressItems method [IMAPI], get_EnumProgressItems method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_enumprogressitems, imapi2fs/IProgressItems::get_EnumProgressItems
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
 - IProgressItems::get_EnumProgressItems
 - imapi2fs/IProgressItems::get_EnumProgressItems
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
 - IProgressItems.get_EnumProgressItems
---

# IProgressItems::get_EnumProgressItems


## -description

Retrieves the list of progress items from the collection.

## -parameters

### -param NewEnum [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a> interface that contains a collection of the progress items contained in the collection.

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

This property returns the same results as the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-get__newenum">IProgressItems::get__NewEnum</a> property and is meant for use by C/C++ applications.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>
