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

# IVPManager::GetVideoPortIndex


## -description



The <code>GetVideoPortIndex</code> method returns the current video port index being used by the Video Port Manager (VPM).




## -parameters




### -param pdwVideoPortIndex [out]

Pointer to a double word containing the index of the video port that the VPM is currently connected to.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns the current video port index being used by the Video Port Manager (VPM).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9064daa7-5868-49a5-9fd6-9a332ab3b470">IVPManager Interface</a>



<a href="https://msdn.microsoft.com/a75332c9-ce3f-4122-ac6c-45478bb5f82c">SetVideoPortIndex</a>
 

 

