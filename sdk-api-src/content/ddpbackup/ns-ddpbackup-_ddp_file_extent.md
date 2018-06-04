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

# _DDP_FILE_EXTENT structure


## -description


<b>DDP_FILE_EXTENT</b> represents the extent of data in a 
     file that is to be read in a pending call to 
     <a href="https://msdn.microsoft.com/9A85B32B-7430-46AC-A9BF-2896651F40AF">ReadBackupFile</a>.


## -struct-fields




### -field Length

Length, in bytes, of the extent.


### -field Offset

Offset, in bytes, from the beginning of the file to the beginning of the extent.


## -remarks



Data Deduplication needs to read only the portions of a container file that back the restore target file.




## -see-also




<a href="https://msdn.microsoft.com/A3AFB530-ED97-4BEC-BF9D-668115E36A36">IDedupReadFileCallback::PreviewContainerRead</a>
 

 

