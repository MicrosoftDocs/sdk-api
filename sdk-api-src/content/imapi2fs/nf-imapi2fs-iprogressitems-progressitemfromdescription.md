---
UID: NF:imapi2fs.IProgressItems.ProgressItemFromDescription
title: IProgressItems::ProgressItemFromDescription (imapi2fs.h)
description: Retrieves a progress item based on the specified file name.
helpviewer_keywords: ["IProgressItems interface [IMAPI]","ProgressItemFromDescription method","IProgressItems.ProgressItemFromDescription","IProgressItems::ProgressItemFromDescription","ProgressItemFromDescription","ProgressItemFromDescription method [IMAPI]","ProgressItemFromDescription method [IMAPI]","IProgressItems interface","imapi.iprogressitems_progressitemfromdescription","imapi2fs/IProgressItems::ProgressItemFromDescription"]
old-location: imapi\iprogressitems_progressitemfromdescription.htm
tech.root: imapi
ms.assetid: c27e9f30-e3f1-4436-b33a-fa3130baf374
ms.date: 12/05/2018
ms.keywords: IProgressItems interface [IMAPI],ProgressItemFromDescription method, IProgressItems.ProgressItemFromDescription, IProgressItems::ProgressItemFromDescription, ProgressItemFromDescription, ProgressItemFromDescription method [IMAPI], ProgressItemFromDescription method [IMAPI],IProgressItems interface, imapi.iprogressitems_progressitemfromdescription, imapi2fs/IProgressItems::ProgressItemFromDescription
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
 - IProgressItems::ProgressItemFromDescription
 - imapi2fs/IProgressItems::ProgressItemFromDescription
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
 - IProgressItems.ProgressItemFromDescription
---

# IProgressItems::ProgressItemFromDescription


## -description

Retrieves a progress item based on the specified file name.

## -parameters

### -param description [in]

String that contains the file name of the progress item to retrieve. The method returns the progress item if this string matches the value for item's description property.

### -param item [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a> interface of the progress item associated with the specified file name.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>description</i> is <b>NULL</b>.

Value:0x80004005

</td>
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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-progressitemfromblock">IProgressItems::ProgressItemFromBlock</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-get_item">IProgressItems::get_Item</a>