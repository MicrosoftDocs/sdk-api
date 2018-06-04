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

# DWM_SOURCE_FRAME_SAMPLING enumeration


## -description


Flags used by the <a href="https://msdn.microsoft.com/75684283-9e5e-4c17-b642-7c309a389f6f">DwmSetPresentParameters</a> function to specify the frame sampling type.


## -enum-fields




### -field DWM_SOURCE_FRAME_SAMPLING_POINT

Use the first source frame that includes the first refresh of the output frame.


### -field DWM_SOURCE_FRAME_SAMPLING_COVERAGE

Use the source frame that includes the most refreshes of the output frame. In the case of multiple source frames with the same coverage, the last frame is used.


### -field DWM_SOURCE_FRAME_SAMPLING_LAST

The maximum recognized <a href="https://msdn.microsoft.com/2574df8f-7562-4034-82c2-def3801e40c4">DWM_SOURCE_FRAME_SAMPLING</a> value, used for validation purposes.

