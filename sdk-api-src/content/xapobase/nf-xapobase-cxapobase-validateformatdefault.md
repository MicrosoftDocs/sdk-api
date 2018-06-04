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

# CXAPOBase::ValidateFormatDefault


## -description


Verifies that an audio format falls within the default ranges supported.


## -parameters




### -param pFormat

Audio format to validate.


### -param fOverwrite

If TRUE indicates that <i>pFormat</i> should be overwritten with the nearest audio format supported if the format it specified is not supported. The nearest audio format is determined by bit depth, framerate and channel count in that order of importance. 


## -returns



Return S_OK if the audio format is supported. Returns XAPO_E_FORMAT_UNSUPPORTED if the audio format is unsupported, <i>pFormat</i> will be overwritten with the nearest audio format if <i>fOverwrite</i> is TRUE. Returns E_INVALIDARG if the audio format is invalid, in which case <i>pFormat</i> will be left untouched.






## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C55C4597-F379-462E-94FE-D7CF2004D8F4">CXAPOBase</a>
 

 

