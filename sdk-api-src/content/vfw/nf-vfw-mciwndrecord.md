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

# MCIWndRecord macro


## -description



The <b>MCIWndRecord</b> macro begins recording content using the MCI device. The recording process begins at the current position in the content and will overwrite existing data for the duration of the recording.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



The function that an MCI device performs during recording depends on the characteristics of the device. An MCI device that uses files, such as a waveform-audio device, sends data to the file during recording. An MCI device that does not use files, such as a video-cassette recorder, receives and externally records data on another medium.



