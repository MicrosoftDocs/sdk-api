---
UID: NF:imapi2fs.IFileSystemImage.Exists
title: IFileSystemImage::Exists method
author: windows-driver-content
description: Checks for the existence of a given file or directory.
old-location: imapi\ifilesystemimage_exists.htm
old-project: imapi
ms.assetid: c3a86e85-1ffd-47c1-9dba-0fc207d76a1a
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Exists method [IMAPI], Exists method [IMAPI], IFileSystemImage interface, Exists,IFileSystemImage.Exists, IFileSystemImage, IFileSystemImage interface [IMAPI], Exists method, IFileSystemImage::Exists, imapi.ifilesystemimage_exists, imapi2fs/IFileSystemImage::Exists
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.Exists
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::Exists method


## -description


Checks for the existence of a given file or directory.


## -parameters




### -param fullPath [in]

String that contains the fully qualified path of the directory or file to check.


### -param itemType [out]

Indicates if the item is a file, a directory, or does not exist. For possible values, see the <a href="https://msdn.microsoft.com/b0ddf0fc-30db-464d-8761-da400386a609">FsiItemType</a> enumeration type.


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
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
The specified path is not fully qualified. The path must begin with '\\' or '/' to indicate the image root, or the images position within a directory structure.

Value: 0xC0AAB110

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object doesn't support this interface.

Value: 0x80004002

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0ddf0fc-30db-464d-8761-da400386a609">FsiItemType</a>



<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

