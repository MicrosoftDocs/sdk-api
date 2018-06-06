---
UID: NF:imapi2fs.IFileSystemImage.put_FileSystemsToCreate
title: IFileSystemImage::put_FileSystemsToCreate
author: windows-sdk-content
description: Sets the file systems to create when generating the result stream.
old-location: imapi\ifilesystemimage_put_filesystemstocreate.htm
old-project: imapi
ms.assetid: c9bb2a86-2bdb-495e-ab5c-479667a211b2
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_FileSystemsToCreate method, IFileSystemImage.put_FileSystemsToCreate, IFileSystemImage::put_FileSystemsToCreate, imapi.ifilesystemimage_put_filesystemstocreate, imapi2fs/IFileSystemImage::put_FileSystemsToCreate, put_FileSystemsToCreate, put_FileSystemsToCreate method [IMAPI], put_FileSystemsToCreate method [IMAPI],IFileSystemImage interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.put_FileSystemsToCreate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::put_FileSystemsToCreate


## -description


Sets the file systems to create when generating the result stream.


## -parameters




### -param newVal [in]

One or more file systems to create when generating the result stream. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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
<dt><b>IMAPI_E_TOO_MANY_DIRS</b></dt>
</dl>
</td>
<td width="60%">
This file system image has too many directories for the <i>%1!ls!</i> file system.

Value: 0xC0AAB130

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
You cannot change the file system specified for creation, because the file system in the imported session and the one in the new session do not match.

Value: 0xC0AAB163L

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
<dt><b>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</b></dt>
</dl>
</td>
<td width="60%">
You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.

Value: 0xC0AAB133

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This feature is not supported for the current file system revision. The image will be created without this feature.

Value: 0x00AAB15FL

</td>
</tr>
</table>
 




## -remarks



This method returns <b>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</b> if the previous session was imported  using <a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a> or <a href="https://msdn.microsoft.com/737f1b5a-be70-4869-9ad0-a1373cb865d9">IFileSystemImage::ImportSpecificFileSystem</a> and the layout of that session is incompatible with the layout used by IMAPI for the file systems identified by the specified <i>newVal</i> in <b>IFileSystemImage::put_FileSystemToCreate</b>.

You can change the file system only when the result stream is not active.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/6f7d2438-5c80-4461-8b48-646f0ca44498">IFileSystemImage::CreateResultImage</a>



<a href="https://msdn.microsoft.com/7350de0b-683a-4363-9233-dbe40f637f2d">IFileSystemImage::get_FileSystemsToCreate</a>
 

 

