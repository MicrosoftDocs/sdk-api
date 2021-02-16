---
UID: NF:imapi2fs.IFsiDirectoryItem.AddDirectory
title: IFsiDirectoryItem::AddDirectory (imapi2fs.h)
description: Adds a directory to the file system image.
helpviewer_keywords: ["AddDirectory","AddDirectory method [IMAPI]","AddDirectory method [IMAPI]","IFsiDirectoryItem interface","IFsiDirectoryItem interface [IMAPI]","AddDirectory method","IFsiDirectoryItem.AddDirectory","IFsiDirectoryItem::AddDirectory","imapi.ifsidirectoryitem_adddirectory","imapi2fs/IFsiDirectoryItem::AddDirectory"]
old-location: imapi\ifsidirectoryitem_adddirectory.htm
tech.root: imapi
ms.assetid: bb716e60-163c-45e7-bdbb-373666cbdc93
ms.date: 12/05/2018
ms.keywords: AddDirectory, AddDirectory method [IMAPI], AddDirectory method [IMAPI],IFsiDirectoryItem interface, IFsiDirectoryItem interface [IMAPI],AddDirectory method, IFsiDirectoryItem.AddDirectory, IFsiDirectoryItem::AddDirectory, imapi.ifsidirectoryitem_adddirectory, imapi2fs/IFsiDirectoryItem::AddDirectory
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
 - IFsiDirectoryItem::AddDirectory
 - imapi2fs/IFsiDirectoryItem::AddDirectory
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
 - IFsiDirectoryItem.AddDirectory
---

# IFsiDirectoryItem::AddDirectory


## -description

Adds a directory to the file system image.

## -parameters

### -param path [in]

String that contains the relative path of directory to create.   

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
</table>

## -remarks

The parent directory for the new subdirectory must already exist within the file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree">IFsiDirectoryItem::AddTree</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove">IFsiDirectoryItem::Remove</a>