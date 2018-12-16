---
UID: NF:xapobase.CXAPOBase.ValidateFormatDefault
title: CXAPOBase::ValidateFormatDefault
author: windows-sdk-content
description: Verifies that an audio format falls within the default ranges supported.
old-location: xaudio2\cxapobase_validateformatdefault.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapobase.CXAPOBase.ValidateFormatDefault(WAVEFORMATEX,BOOL)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CXAPOBase interface [XAudio2 Audio Mixing APIs],ValidateFormatDefault method, CXAPOBase.ValidateFormatDefault, CXAPOBase::ValidateFormatDefault, ValidateFormatDefault, ValidateFormatDefault method [XAudio2 Audio Mixing APIs], ValidateFormatDefault method [XAudio2 Audio Mixing APIs],CXAPOBase interface, xapobase/CXAPOBase::ValidateFormatDefault, xaudio2.cxapobase_validateformatdefault
ms.topic: method
req.header: xapobase.h
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
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOBase.ValidateFormatDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Ee415236(v=VS.85).aspx">CXAPOBase</a>
 

 

