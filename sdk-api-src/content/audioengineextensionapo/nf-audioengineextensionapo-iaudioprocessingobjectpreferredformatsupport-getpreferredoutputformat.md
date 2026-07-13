---
UID: NF:audioengineextensionapo.IAudioProcessingObjectPreferredFormatSupport.GetPreferredOutputFormat
tech.root: audio
title: IAudioProcessingObjectPreferredFormatSupport::GetPreferredOutputFormat
ms.date: 08/28/2023
targetos: Windows
description: Callback function that allows APOs to specify a preferred output format for the provided input format.
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
 - IAudioProcessingObjectPreferredFormatSupport::GetPreferredOutputFormat
f1_keywords:
 - IAudioProcessingObjectPreferredFormatSupport::GetPreferredOutputFormat
 - audioengineextensionapo/IAudioProcessingObjectPreferredFormatSupport::GetPreferredOutputFormat
dev_langs:
 - c++
helpviewer_keywords:
 - GetPreferredOutputFormat
---

## -description

Callback function that allows APOs to specify a preferred output format for the provided input format.

## -parameters

### -param inputFormat [in]

An [IAudioMediaType](../audiomediatype/nn-audiomediatype-iaudiomediatype.md) representing the input format associated with the callback.

### -param preferredFormat [out]

An **IAudioMediaType** representing the preferred input format for the APO.

## -returns

An HRESULT.

## -remarks

## -see-also

