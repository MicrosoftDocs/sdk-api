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

# IBackgroundCopyFile::GetProgress


## -description


Retrieves information on the progress of the file transfer.


## -parameters




### -param pVal






#### - pProgress [out]

Structure whose members indicate the progress of the file transfer. For details on the type of progress information available, see the 
<a href="https://msdn.microsoft.com/322363b4-081e-4100-9087-e34c21a3ffae">BG_FILE_PROGRESS</a> structure. 


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/322363b4-081e-4100-9087-e34c21a3ffae">BG_FILE_PROGRESS</a>



<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">IBackgroundCopyJob::GetProgress</a>
 

 

