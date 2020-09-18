---
UID: NF:imapi2fs.IFsiDirectoryItem.AddTree
title: IFsiDirectoryItem::AddTree (imapi2fs.h)
description: Adds the contents of a directory tree to the file system image.
helpviewer_keywords: ["AddTree","AddTree method [IMAPI]","AddTree method [IMAPI]","IFsiDirectoryItem interface","IFsiDirectoryItem interface [IMAPI]","AddTree method","IFsiDirectoryItem.AddTree","IFsiDirectoryItem::AddTree","imapi.ifsidirectoryitem_addtree","imapi2fs/IFsiDirectoryItem::AddTree"]
old-location: imapi\ifsidirectoryitem_addtree.htm
tech.root: imapi
ms.assetid: 4f36538c-fba7-4a0c-a2e9-443b7dc2fdab
ms.date: 12/05/2018
ms.keywords: AddTree, AddTree method [IMAPI], AddTree method [IMAPI],IFsiDirectoryItem interface, IFsiDirectoryItem interface [IMAPI],AddTree method, IFsiDirectoryItem.AddTree, IFsiDirectoryItem::AddTree, imapi.ifsidirectoryitem_addtree, imapi2fs/IFsiDirectoryItem::AddTree
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
 - IFsiDirectoryItem::AddTree
 - imapi2fs/IFsiDirectoryItem::AddTree
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
 - IFsiDirectoryItem.AddTree
---

# IFsiDirectoryItem::AddTree


## -description

Adds the contents of a directory tree to the file system image.

## -parameters

### -param sourceDirectory [in]

String that contains the relative path of the directory tree to create.

Specify the full path when calling this method from the root directory item.

### -param includeBaseDirectory [in]

Set to VARIANT_TRUE to include the directory in <i>sourceDirectory</i> as a subdirectory in the file system image. Otherwise, VARIANT_FALSE.

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
<dt><b>IMAPI_E_DIRECTORY_READ_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Failure enumerating files in the directory tree is inaccessible due to permissions.

Value: 0xC0AAB12BL

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DATA_STREAM_CREATE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
One or more  of the files in the directory tree is inaccessible due to permissions.

Value: 0xC0AAB12A

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
</table>
 

<div class="alert"><b>Note</b>  Values returned by the  <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> functions may also be returned here.</div>
<div> </div>

## -remarks

The parent directory for the new subdirectory must already exist within the file system image.


The subdirectory structure within specified source directory is implicitly mirrored in the file system image.  

If file or directory collisions occur, the content of the specified source directory prevails. The file system image is overwritten with the appropriate directories and files from the source directory.

If an exception occurs during processing, the file system image reverts to its previous state.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-adddirectory">IFsiDirectoryItem::AddDirectory</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove">IFsiDirectoryItem::Remove</a>