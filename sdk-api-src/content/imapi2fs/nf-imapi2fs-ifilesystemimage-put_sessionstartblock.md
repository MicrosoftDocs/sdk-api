---
UID: NF:imapi2fs.IFileSystemImage.put_SessionStartBlock
title: IFileSystemImage::put_SessionStartBlock
author: windows-sdk-content
description: Sets the starting block address for the recording session.
old-location: imapi\ifilesystemimage_put_sessionstartblock.htm
old-project: imapi
ms.assetid: 0018d614-c936-41f1-8700-477aa259da2a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_SessionStartBlock method, IFileSystemImage.put_SessionStartBlock, IFileSystemImage::put_SessionStartBlock, imapi.ifilesystemimage_put_sessionstartblock, imapi2fs/IFileSystemImage::put_SessionStartBlock, put_SessionStartBlock, put_SessionStartBlock method [IMAPI], put_SessionStartBlock method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage.put_SessionStartBlock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::put_SessionStartBlock


## -description


Sets the starting block address for the recording session.


## -parameters




### -param newVal [in]

Block number of the new recording session.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



If the previous session is imported, the session start block cannot be changed manually.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/0f1faea7-4272-42da-afdf-3399c9dd629f">IFileSystemImage::get_SessionStartBlock</a>
 

 

