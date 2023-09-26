---
UID: NF:audioengineextensionapo.IAudioProcessingObjectPreferredFormatSupport.GetPreferredInputFormat
tech.root: audio
title: IAudioProcessingObjectPreferredFormatSupport::GetPreferredInputFormat
ms.date: 08/28/2023
targetos: Windows
description: Callback function that allows APOs to specify a preferred input format for the provided output format.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 23H2
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectPreferredFormatSupport::GetPreferredInputFormat
f1_keywords:
 - IAudioProcessingObjectPreferredFormatSupport::GetPreferredInputFormat
 - audioengineextensionapo/IAudioProcessingObjectPreferredFormatSupport::GetPreferredInputFormat
dev_langs:
 - c++
helpviewer_keywords:
 - GetPreferredInputFormat
---

## -description

Callback function that allows APOs to specify a preferred input format for the provided output format.

## -parameters

### -param outputFormat [in]

An [IAudioMediaType](../audiomediatype/nn-audiomediatype-iaudiomediatype.md) representing the output format associated with the callback.

### -param preferredFormat [out]

An **IAudioMediaType** representing the preferred input format for the APO.

## -returns

An HRESULT.

## -remarks

This API enables scenarios such as a headphone provider that provides virtual surround sound. The APO could request to receive 7-1 input even though the endpoint renders in stereo. APOs can specify different preferred formats for different output formats. For example, an app may request 7.1 input when the m stream type is media, but request stereo input when the stream type is communications.

## -see-also

