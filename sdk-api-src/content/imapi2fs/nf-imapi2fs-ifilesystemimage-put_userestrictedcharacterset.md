---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFileSystemImage::put_UseRestrictedCharacterSet


## -description


Determines if file and directory names should be restricted to using only CP_ANSI characters. <div class="alert"><b>Note</b>  <b>IFileSystemImage::put_UseRestrictedCharacterSet</b> has been deprecated. Implementing this method is not recommended.</div>
<div> </div>



## -parameters




### -param newVal [in]

Set to VARIANT_TRUE to restrict file and directory names to use only CP_ANSI characters. Otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



Setting this property does not affect files or directories already in the file system image.

You can change the value of this property only when the result stream is not active.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">IFileSystemImage::CreateDirectoryItem</a>



<a href="https://msdn.microsoft.com/8e90e367-e7c3-41db-a8c9-9b0220cf402b">IFileSystemImage::CreateFileItem</a>



<a href="https://msdn.microsoft.com/106615e8-f1d4-4ac9-b96a-bcda204f5e2c">IFileSystemImage::get_UseRestrictedCharacterSet</a>
 

 

