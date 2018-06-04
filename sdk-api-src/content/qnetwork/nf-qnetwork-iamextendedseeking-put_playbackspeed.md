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

# IAMExtendedSeeking::put_PlaybackSpeed


## -description



The <code>put_PlaybackSpeed</code> method specifies the playback speed.




## -parameters




### -param Speed [in]

Specifies the playback speed. The value may be positive or negative, but not zero.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e0e49af-61ef-408c-8c26-bb29ab26a1f5">IAMExtendedSeeking Interface</a>



<a href="https://msdn.microsoft.com/a92309fb-185a-4d6c-81c2-9613634c7170">IAMExtendedSeeking::get_PlaybackSpeed</a>
 

 

