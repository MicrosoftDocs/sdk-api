---
UID: NF:imapi2fs.IFileSystemImage.get_UseRestrictedCharacterSet
title: IFileSystemImage::get_UseRestrictedCharacterSet
author: windows-sdk-content
description: Determines if the file and directory names use a restricted character.
old-location: imapi\ifilesystemimage_get_userestrictedcharacterset.htm
old-project: imapi
ms.assetid: 106615e8-f1d4-4ac9-b96a-bcda204f5e2c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UseRestrictedCharacterSet method, IFileSystemImage.get_UseRestrictedCharacterSet, IFileSystemImage::get_UseRestrictedCharacterSet, get_UseRestrictedCharacterSet, get_UseRestrictedCharacterSet method [IMAPI], get_UseRestrictedCharacterSet method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_userestrictedcharacterset, imapi2fs/IFileSystemImage::get_UseRestrictedCharacterSet
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
 - IFileSystemImage.get_UseRestrictedCharacterSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_UseRestrictedCharacterSet


## -description


Determines if the file and directory names use a restricted character.


## -parameters




### -param pVal [out]

Is VARIANT_TRUE if the file and directory names to add to the file system image must consist of characters that map directly to CP_ANSI (code points 32 through 127). Otherwise, VARIANT_FALSE.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">IFileSystemImage::CreateDirectoryItem</a>



<a href="https://msdn.microsoft.com/8e90e367-e7c3-41db-a8c9-9b0220cf402b">IFileSystemImage::CreateFileItem</a>



<a href="https://msdn.microsoft.com/de64ef3d-94b3-4d97-946e-8331c5a39f4b">IFileSystemImage::put_UseRestrictedCharacterSet</a>
 

 

