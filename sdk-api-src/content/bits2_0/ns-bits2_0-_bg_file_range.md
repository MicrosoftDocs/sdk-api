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

# _BG_FILE_RANGE structure


## -description


The <b>BG_FILE_RANGE</b> structure identifies a range of bytes to download from a file.


## -struct-fields




### -field InitialOffset

Zero-based offset to the beginning of the range of bytes to download from a file.


### -field Length

The length of the range, in bytes. Do not specify a zero byte length. To indicate that the range extends to the end of the file, specify <b>BG_LENGTH_TO_EOF</b>. 


## -remarks



The range must exist in the file or BITS generates an <b>BG_E_INVALID_RANGE</b> error.




## -see-also




<a href="https://msdn.microsoft.com/2e0ea08e-5f97-45c9-9280-ce6c4dce7a17">IBackgroundCopyFile2::GetFileRanges</a>



<a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a>
 

 

