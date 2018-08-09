---
UID: NF:imapi2fs.IFileSystemImage.get_FileCount
title: IFileSystemImage::get_FileCount
author: windows-sdk-content
description: Retrieves the number of files in the file system image.
old-location: imapi\ifilesystemimage_get_filecount.htm
old-project: imapi
ms.assetid: b2545f85-84c9-4f01-98d7-fd6b37fcda5a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FileCount method, IFileSystemImage.get_FileCount, IFileSystemImage::get_FileCount, get_FileCount, get_FileCount method [IMAPI], get_FileCount method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_filecount, imapi2fs/IFileSystemImage::get_FileCount
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
 - IFileSystemImage.get_FileCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_FileCount


## -description


Retrieves the number of files in the file system image.


## -parameters




### -param pVal [out]

Number of files in the file system image.


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
 

 

