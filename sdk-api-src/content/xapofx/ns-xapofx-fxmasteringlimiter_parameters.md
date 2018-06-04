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

# FXMASTERINGLIMITER_PARAMETERS structure


## -description


Parameters for use with the <a href="https://msdn.microsoft.com/762062de-4e19-5e42-8059-e2f8741bd362">FXMasteringLimiter  XAPO</a>.


## -struct-fields




### -field Release

Speed, in milliseconds, at which the limiter stops affecting audio after the audio drops below the limiter's threshold, which is specified by the <b>Loudness</b> member. This value must be between <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_MIN_RELEASE (1)</a> and <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_MAX_RELEASE (20)</a> and defaults to <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_DEFAULT_RELEASE (6)</a>.



### -field Loudness

Loudness metric threshold of the limiter. This value must be between <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_MIN_LOUDNESS (1)</a> and <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_MAX_LOUDNESS (1800)</a> and defaults to <a href="fxmasteringlimit_constants.htm">FXMASTERINGLIMITER_DEFAULT_LOUDNESS (1000)</a>.



## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

