---
UID: NF:imapi2fs.IFsiDirectoryItem.Remove
title: IFsiDirectoryItem::Remove (imapi2fs.h)
description: Removes the specified item from the file system image.
helpviewer_keywords: ["IFsiDirectoryItem interface [IMAPI]","Remove method","IFsiDirectoryItem.Remove","IFsiDirectoryItem::Remove","Remove","Remove method [IMAPI]","Remove method [IMAPI]","IFsiDirectoryItem interface","imapi.ifsidirectoryitem_remove","imapi2fs/IFsiDirectoryItem::Remove"]
old-location: imapi\ifsidirectoryitem_remove.htm
tech.root: imapi
ms.assetid: bbd45185-439a-4847-8481-7139e81b34fd
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],Remove method, IFsiDirectoryItem.Remove, IFsiDirectoryItem::Remove, Remove, Remove method [IMAPI], Remove method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_remove, imapi2fs/IFsiDirectoryItem::Remove
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
 - IFsiDirectoryItem::Remove
 - imapi2fs/IFsiDirectoryItem::Remove
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
 - IFsiDirectoryItem.Remove
---

# IFsiDirectoryItem::Remove


## -description

Removes the specified item from the file system image.

## -parameters

### -param path [in]

String that contains the relative path of the item to remove.
The path is relative to current directory item.

Specify the full path when calling this method from the root directory item.

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
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
Path '%1!s!' is badly formed or contains invalid characters.

Value: 0xC0AAB110

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>	IMAPI_E_NOT_IN_FILE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
<i>ls!'</i> is not part of the file system. It must be added to complete this operation.

Value: 0xC0AAB10B

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DIR_NOT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The directory <i>%1!s!</i> is not empty.

Value: 0xC0AAB10A

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: <i>%1!ls!</i>.

Value: 0xC0AAB100

</td>
</tr>
</table>

## -remarks

This method is only callable on directory items present in the file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-adddirectory">IFsiDirectoryItem::AddDirectory</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree">IFsiDirectoryItem::RemoveTree</a>