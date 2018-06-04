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

# IAudioLfxControl::SetLocalEffectsState


## -description


The <b>SetLocalEffectsState</b> method sets the local effects state that is to be  applied to the offloaded audio stream.


## -parameters




### -param bEnabled [in]

Indicates the local effects state that is to be applied to the offloaded audio stream. A value of <b>TRUE</b> enables  local effects, and the local effects in the audio graph are applied to the stream. A value of <b>FALSE</b> disables local effects, so that the  local effects in the audio graph are not applied to the audio stream.


## -returns



The <b>SetLocalEffectsState</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/E4290AE9-7F2E-4D0B-BEAF-F01D95B3E03D">IAudioLfxControl</a>
 

 

