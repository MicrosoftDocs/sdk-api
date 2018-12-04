---
UID: NF:imapi2fs.IFileSystemImage.get_SessionStartBlock
title: IFileSystemImage::get_SessionStartBlock
author: windows-sdk-content
description: Retrieves the starting block address for the recording session.
old-location: imapi\ifilesystemimage_get_sessionstartblock.htm
tech.root: imapi
ms.assetid: 0f1faea7-4272-42da-afdf-3399c9dd629f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_SessionStartBlock method, IFileSystemImage.get_SessionStartBlock, IFileSystemImage::get_SessionStartBlock, get_SessionStartBlock, get_SessionStartBlock method [IMAPI], get_SessionStartBlock method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_sessionstartblock, imapi2fs/IFileSystemImage::get_SessionStartBlock
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
 - IFileSystemImage.get_SessionStartBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::get_SessionStartBlock


## -description


Retrieves the starting block address for the recording session.


## -parameters




### -param pVal [out]

Starting block address for the recording session.


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
 




## -remarks



The session starting block can be set in the following ways:

<ul>
<li>Importing a file system automatically sets the session starting block.</li>
<li>If the previous session is not imported, the client can call <a href="https://msdn.microsoft.com/0018d614-c936-41f1-8700-477aa259da2a">IFileSystemImage::put_SessionStartBlock</a> to set this property.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>



<a href="https://msdn.microsoft.com/737f1b5a-be70-4869-9ad0-a1373cb865d9">IFileSystemImage::ImportSpecificFileSystem</a>
 

 

