---
UID: NF:imapi2fs.IFsiDirectoryItem.AddFile
title: IFsiDirectoryItem::AddFile (imapi2fs.h)
description: Adds a file to the file system image.
helpviewer_keywords: ["AddFile","AddFile method [IMAPI]","AddFile method [IMAPI]","IFsiDirectoryItem interface","IFsiDirectoryItem interface [IMAPI]","AddFile method","IFsiDirectoryItem.AddFile","IFsiDirectoryItem::AddFile","imapi.ifsidirectoryitem_addfile","imapi2fs/IFsiDirectoryItem::AddFile"]
old-location: imapi\ifsidirectoryitem_addfile.htm
tech.root: imapi
ms.assetid: 82f62372-3c79-4bf5-a723-cd09a5444ffc
ms.date: 12/05/2018
ms.keywords: AddFile, AddFile method [IMAPI], AddFile method [IMAPI],IFsiDirectoryItem interface, IFsiDirectoryItem interface [IMAPI],AddFile method, IFsiDirectoryItem.AddFile, IFsiDirectoryItem::AddFile, imapi.ifsidirectoryitem_addfile, imapi2fs/IFsiDirectoryItem::AddFile
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
 - IFsiDirectoryItem::AddFile
 - imapi2fs/IFsiDirectoryItem::AddFile
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
 - IFsiDirectoryItem.AddFile
---

# IFsiDirectoryItem::AddFile


## -description

Adds a file to the file system image.

## -parameters

### -param path [in]

String that contains the relative path of the directory to contain the new file.

Specify the full path when calling this method from the root directory item.

### -param fileData [in]

An <b>IStream</b> interface of the file (data stream) to write to the media.

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

The directory that will contain the new file must already exist within the file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-adddirectory">IFsiDirectoryItem::AddDirectory</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove">IFsiDirectoryItem::Remove</a>