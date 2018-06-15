---
UID: NS:xapofx.FXMASTERINGLIMITER_PARAMETERS
title: FXMASTERINGLIMITER_PARAMETERS
author: windows-sdk-content
description: Parameters for use with the FXMasteringLimiter XAPO.
old-location: xaudio2\fxmasteringlimiter_parameters.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXMASTERINGLIMITER_PARAMETERS
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: FXMASTERINGLIMITER_PARAMETERS, FXMASTERINGLIMITER_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapofx/FXMASTERINGLIMITER_PARAMETERS, xaudio2.fxmasteringlimiter_parameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xapofx.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: FXMASTERINGLIMITER_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapofx.h
api_name:
 - FXMASTERINGLIMITER_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# FXMASTERINGLIMITER_PARAMETERS structure


## -description


Parameters for use with the <a href="https://msdn.microsoft.com/762062de-4e19-5e42-8059-e2f8741bd362">FXMasteringLimiter  XAPO</a>.


## -struct-fields




### -field Release

Speed, in milliseconds, at which the limiter stops affecting audio after the audio drops below the limiter's threshold, which is specified by the <b>Loudness</b> member. This value must be between <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_MIN_RELEASE+(1)">FXMASTERINGLIMITER_MIN_RELEASE (1)</a> and <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_MAX_RELEASE+(20)">FXMASTERINGLIMITER_MAX_RELEASE (20)</a> and defaults to <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_DEFAULT_RELEASE+(6)">FXMASTERINGLIMITER_DEFAULT_RELEASE (6)</a>.



### -field Loudness

Loudness metric threshold of the limiter. This value must be between <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_MIN_LOUDNESS+(1)">FXMASTERINGLIMITER_MIN_LOUDNESS (1)</a> and <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_MAX_LOUDNESS+(1800)">FXMASTERINGLIMITER_MAX_LOUDNESS (1800)</a> and defaults to <a href="https://www.bing.com/search?q=FXMASTERINGLIMITER_DEFAULT_LOUDNESS+(1000)">FXMASTERINGLIMITER_DEFAULT_LOUDNESS (1000)</a>.



## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

