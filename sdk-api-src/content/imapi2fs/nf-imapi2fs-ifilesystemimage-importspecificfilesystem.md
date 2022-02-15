---
UID: NF:imapi2fs.IFileSystemImage.ImportSpecificFileSystem
title: IFileSystemImage::ImportSpecificFileSystem (imapi2fs.h)
description: Import a specific file system from disc.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","ImportSpecificFileSystem method","IFileSystemImage.ImportSpecificFileSystem","IFileSystemImage::ImportSpecificFileSystem","ImportSpecificFileSystem","ImportSpecificFileSystem method [IMAPI]","ImportSpecificFileSystem method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_importspecificfilesystem","imapi2fs/IFileSystemImage::ImportSpecificFileSystem"]
old-location: imapi\ifilesystemimage_importspecificfilesystem.htm
tech.root: imapi
ms.assetid: 737f1b5a-be70-4869-9ad0-a1373cb865d9
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],ImportSpecificFileSystem method, IFileSystemImage.ImportSpecificFileSystem, IFileSystemImage::ImportSpecificFileSystem, ImportSpecificFileSystem, ImportSpecificFileSystem method [IMAPI], ImportSpecificFileSystem method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_importspecificfilesystem, imapi2fs/IFileSystemImage::ImportSpecificFileSystem
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
 - IFileSystemImage::ImportSpecificFileSystem
 - imapi2fs/IFileSystemImage::ImportSpecificFileSystem
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
 - IFileSystemImage.ImportSpecificFileSystem
---

# IFileSystemImage::ImportSpecificFileSystem


## -description

Import a specific file system from disc.

## -parameters

### -param fileSystemToUse [in]

Identifies the file system to import. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

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
<dt><b>IMAPI_E_MULTISESSION_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
MultisessionInterfaces property must be set prior calling this method.

Value: 0xC0AAB15D

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_OBJECT_CONFLICT</b></dt>
</dl>
</td>
<td width="60%">
A boot object can only be included in an initial disc image.

Value: 0xC0AAB149

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_EMPTY_DISC</b></dt>
</dl>
</td>
<td width="60%">
Optical media is empty.

Value: 0xC0AAB150

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
<dt><b>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</b></dt>
</dl>
</td>
<td width="60%">
IMAPI supports none of the multisession type(s) provided on the current media.

Value: 0xC0AAB15C

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">IFileSystemImage::ImportFileSystem</a>  method returns this error if there is no media in the recording device.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</b></dt>
</dl>
</td>
<td width="60%">
Operation failed because of incompatible layout of the previous session imported from the medium.

Value: 0xC0AAB133

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FILE_SYSTEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified disc does not contain a '%1!ls!' file system.

Value: 0xC0AAB152

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
The file system specified for import contains an invalid file name.

Value: 0xC0AAB110

</td>
</tr>
</table>

## -remarks

You must call <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces">IFileSystemImage::put_MultisessionInterfaces</a> prior to calling <b>IFileSystemImage::ImportSpecificFileSystem</b>. Additionally, it is recommended that  <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank">IDiscFormat2::get_MediaHeuristicallyBlank</a> is called before <b>IFileSystemImage::put_MultisessionInterfaces</b> to verify that the media is not blank.

You may call this method at any time during the construction of the in-memory file system.  If, during import, a file or directory already exists in the in-memory copy, the in-memory version will be retained; the imported file will be discarded.

On re-writable media (DVD+/-RW, DVDRAM, BD-RE), import or burning a second session is not support if the first session has an ISO9660 file system, due to file system limitations.

This method only reads the file information. If the item is a file, the file data is copied when calling <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>, <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree">IFsiDirectoryItem::AddTree</a>, or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a> method. 

this method returns <b>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</b> if the layout of the file system  in the last session is incompatible with the layout used by IMAPI for the creation of requested file systems for the result image. For more details see the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">IFileSystemImage::put_FileSystemsToCreate</a> method documentation.
If the file system specified by <i>fileSystemToUse</i> has not been found, this method returns <b>IMAPI_E_FILE_SYSTEM_NOT_FOUND</b>.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>