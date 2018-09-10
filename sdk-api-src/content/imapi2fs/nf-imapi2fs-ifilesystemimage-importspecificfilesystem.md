---
UID: NF:imapi2fs.IFileSystemImage.ImportSpecificFileSystem
title: IFileSystemImage::ImportSpecificFileSystem
author: windows-sdk-content
description: Import a specific file system from disc.
old-location: imapi\ifilesystemimage_importspecificfilesystem.htm
tech.root: imapi
ms.assetid: 737f1b5a-be70-4869-9ad0-a1373cb865d9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage interface [IMAPI],ImportSpecificFileSystem method, IFileSystemImage.ImportSpecificFileSystem, IFileSystemImage::ImportSpecificFileSystem, ImportSpecificFileSystem, ImportSpecificFileSystem method [IMAPI], ImportSpecificFileSystem method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_importspecificfilesystem, imapi2fs/IFileSystemImage::ImportSpecificFileSystem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.ImportSpecificFileSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::ImportSpecificFileSystem


## -description


Import a specific file system from disc.


## -parameters




### -param fileSystemToUse [in]

Identifies the file system to import. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>  method returns this error if there is no media in the recording device.</div>
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



You must call <a href="https://msdn.microsoft.com/632cd123-4e66-4ac3-891a-aa9d0c085b4f">IFileSystemImage::put_MultisessionInterfaces</a> prior to calling <b>IFileSystemImage::ImportSpecificFileSystem</b>. Additionally, it is recommended that  <a href="https://msdn.microsoft.com/28c410cc-5135-4443-8b86-e34676f14f51">IDiscFormat2::get_MediaHeuristicallyBlank</a> is called before <b>IFileSystemImage::put_MultisessionInterfaces</b> to verify that the media is not blank.

You may call this method at any time during the construction of the in-memory file system.  If, during import, a file or directory already exists in the in-memory copy, the in-memory version will be retained; the imported file will be discarded.

On re-writable media (DVD+/-RW, DVDRAM, BD-RE), import or burning a second session is not support if the first session has an ISO9660 file system, due to file system limitations.

This method only reads the file information. If the item is a file, the file data is copied when calling <a href="https://msdn.microsoft.com/82f62372-3c79-4bf5-a723-cd09a5444ffc">IFsiDirectoryItem::AddFile</a>, <a href="https://msdn.microsoft.com/4f36538c-fba7-4a0c-a2e9-443b7dc2fdab">IFsiDirectoryItem::AddTree</a>, or <a href="https://msdn.microsoft.com/f4855907-89e5-4127-9307-35970046a236">IFsiDirectoryItem::Add</a> method. 

this method returns <b>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</b> if the layout of the file system  in the last session is incompatible with the layout used by IMAPI for the creation of requested file systems for the result image. For more details see the <a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a> method documention.
If the file system specified by <i>fileSystemToUse</i> has not been found, this method returns <b>IMAPI_E_FILE_SYSTEM_NOT_FOUND</b>.





## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

