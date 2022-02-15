---
UID: NF:imapi2fs.IFsiDirectoryItem.Add
title: IFsiDirectoryItem::Add (imapi2fs.h)
description: Adds a file or directory described by the IFsiItem object to the file system image.
helpviewer_keywords: ["Add","Add method [IMAPI]","Add method [IMAPI]","IFsiDirectoryItem interface","IFsiDirectoryItem interface [IMAPI]","Add method","IFsiDirectoryItem.Add","IFsiDirectoryItem::Add","imapi.ifsidirectoryitem_add","imapi2fs/IFsiDirectoryItem::Add"]
old-location: imapi\ifsidirectoryitem_add.htm
tech.root: imapi
ms.assetid: f4855907-89e5-4127-9307-35970046a236
ms.date: 12/05/2018
ms.keywords: Add, Add method [IMAPI], Add method [IMAPI],IFsiDirectoryItem interface, IFsiDirectoryItem interface [IMAPI],Add method, IFsiDirectoryItem.Add, IFsiDirectoryItem::Add, imapi.ifsidirectoryitem_add, imapi2fs/IFsiDirectoryItem::Add
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
 - IFsiDirectoryItem::Add
 - imapi2fs/IFsiDirectoryItem::Add
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
 - IFsiDirectoryItem.Add
---

# IFsiDirectoryItem::Add


## -description

Adds a file or directory described by the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a> object to the file system image.

## -parameters

### -param item [in]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a> interface of the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a> or <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a> to add to the file system  image.

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
<dt><b>IMAPI_E_DATA_STREAM_READ_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Cannot read data from stream supplied for file '%1!ls!'.

Value: 0xC0AAB129

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DUP_NAME</b></dt>
</dl>
</td>
<td width="60%">
ls!' name already exists.

Value: 0xC0AAB112

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_NO_UNIQUE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Attempt to add '%1!ls!' failed:  cannot create a file-system-specific unique name for the %2!ls! file system.

Value: 0xC0AAB113

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGE_SIZE_LIMIT</b></dt>
</dl>
</td>
<td width="60%">
Adding '%1!ls!' would result in a result image having a size larger than the current configured limit.

Value: 0xC0AAB120

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_ISO9660_LEVELS</b></dt>
</dl>
</td>
<td width="60%">
ISO9660 is limited to 8 levels of directories.

Value: 0xC0AAB131

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_TOO_MANY_DIRS</b></dt>
</dl>
</td>
<td width="60%">
This file system image has too many directories for the %1!ls! file system.

Value: 0xC0AAB130

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DIR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The directory '%1!s!' not found in FileSystemImage hierarchy.

Value: 0xC0AAB11A

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>	IMAPI_E_NOT_IN_FILE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
This file or directory is not part of the file system. It must be added to complete this operation.

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
<dt><b>IMAPI_E_IMAGE_SIZE_LIMIT
</b></dt>
</dl>
</td>
<td width="60%">
Adding this file or directory would result in a result image having a size larger than the current configured limit.


Value: 0xC0AAB120

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
 

<div class="alert"><b>Note</b>  Values returned by the  IUnknown::QueryInterface method may also be returned here.</div>
<div> </div>

## -remarks

To create a directory item or file item, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">IFileSystemImage::CreateDirectoryItem</a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem">IFileSystemImage::CreateFileItem</a> method, respectively.

Once an item is added to the file system image, the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_data">IFsiFileItem::get_Data</a> property becomes read-only.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-adddirectory">IFsiDirectoryItem::AddDirectory</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove">IFsiDirectoryItem::Remove</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>