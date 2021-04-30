---
UID: NF:xapobase.CXAPOBase.ValidateFormatPair
title: CXAPOBase::ValidateFormatPair (xapobase.h)
description: Verifies that an input and output format pair configuration is supported by the XAPO.
helpviewer_keywords: ["CXAPOBase interface [XAudio2 Audio Mixing APIs]","ValidateFormatPair method","CXAPOBase.ValidateFormatPair","CXAPOBase::ValidateFormatPair","ValidateFormatPair","ValidateFormatPair method [XAudio2 Audio Mixing APIs]","ValidateFormatPair method [XAudio2 Audio Mixing APIs]","CXAPOBase interface","xapobase/CXAPOBase::ValidateFormatPair","xaudio2.cxapobase_validateformatpair"]
old-location: xaudio2\cxapobase_validateformatpair.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapobase.CXAPOBase.ValidateFormatPair(const WAVEFORMATEX,WAVEFORMATEX,BOOL)
ms.date: 12/05/2018
ms.keywords: CXAPOBase interface [XAudio2 Audio Mixing APIs],ValidateFormatPair method, CXAPOBase.ValidateFormatPair, CXAPOBase::ValidateFormatPair, ValidateFormatPair, ValidateFormatPair method [XAudio2 Audio Mixing APIs], ValidateFormatPair method [XAudio2 Audio Mixing APIs],CXAPOBase interface, xapobase/CXAPOBase::ValidateFormatPair, xaudio2.cxapobase_validateformatpair
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CXAPOBase::ValidateFormatPair
 - xapobase/CXAPOBase::ValidateFormatPair
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOBase.ValidateFormatPair
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

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapobase">CXAPOBase</a>