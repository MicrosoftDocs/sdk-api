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

# IAudioLfxControl::GetLocalEffectsState


## -description


The <b>GetLocalEffectsState</b> method retrieves the local effects state that is currently applied to the offloaded audio stream.


## -parameters




### -param pbEnabled [out]

A pointer to the Boolean variable that indicates the state of the local effects that have been applied to the offloaded audio stream. A value of <b>TRUE</b> indicates that local effects have been enabled and applied to the stream. A value of <b>FALSE</b> indicates that local effects have been disabled.


## -returns



The <b>GetLocalEffectsState</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/E4290AE9-7F2E-4D0B-BEAF-F01D95B3E03D">IAudioLfxControl</a>
 

 

