---
UID: NF:xapobase.CXAPOBase.ValidateFormatPair
title: CXAPOBase::ValidateFormatPair
author: windows-sdk-content
description: Verifies that an input and output format pair configuration is supported by the XAPO.
old-location: xaudio2\cxapobase_validateformatpair.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapobase.CXAPOBase.ValidateFormatPair(const WAVEFORMATEX,WAVEFORMATEX,BOOL)
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: CXAPOBase interface [XAudio2 Audio Mixing APIs],ValidateFormatPair method, CXAPOBase.ValidateFormatPair, CXAPOBase::ValidateFormatPair, ValidateFormatPair, ValidateFormatPair method [XAudio2 Audio Mixing APIs], ValidateFormatPair method [XAudio2 Audio Mixing APIs],CXAPOBase interface, xapobase/CXAPOBase::ValidateFormatPair, xaudio2.cxapobase_validateformatpair
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XAPO_REGISTRATION_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	XAPOBase.lib
-	XAPOBase.dll
api_name:
-	CXAPOBase.ValidateFormatPair
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOBase::ValidateFormatPair


## -description


Verifies that an input and output format pair configuration is supported by the XAPO.


## -parameters




### -param pSupportedFormat

An audio format known to be supported by the XAPO.


### -param pRequestedFormat

An audio format to examine, must be a pointer to a WAVEFORMATEXTENSIBLE structure if <i>fOverWrite</i> is TRUE.


### -param fOverwrite

If TRUE indicates that <i>pRequestedFormat</i> should be overwritten with the nearest audio format supported if the requested format is not supported. The nearest audio format is determined by bit depth, framerate and channel count in that order of importance.


## -returns



Returns S_OK if the format pair is supported. Returns XAPO_E_FORMAT_UNSUPPORTED if the format pair is unsupported; <i>pRequestedFormat</i> will be overwritten if <i>fOverWrite</i> is TRUE. Returns E_INVALIDARG if either audio format was invalid; <i>pRequestedFormat</i> will be left untouched.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C55C4597-F379-462E-94FE-D7CF2004D8F4">CXAPOBase</a>
 

 

