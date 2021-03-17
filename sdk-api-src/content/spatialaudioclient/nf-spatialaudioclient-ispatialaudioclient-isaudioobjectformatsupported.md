---
UID: NF:spatialaudioclient.ISpatialAudioClient.IsAudioObjectFormatSupported
title: ISpatialAudioClient::IsAudioObjectFormatSupported (spatialaudioclient.h)
description: Gets a value indicating whether ISpatialAudioObjectRenderStream supports a the specified format.
helpviewer_keywords: ["ISpatialAudioClient interface [Core Audio]","IsAudioObjectFormatSupported method","ISpatialAudioClient.IsAudioObjectFormatSupported","ISpatialAudioClient::IsAudioObjectFormatSupported","IsAudioObjectFormatSupported","IsAudioObjectFormatSupported method [Core Audio]","IsAudioObjectFormatSupported method [Core Audio]","ISpatialAudioClient interface","coreaudio.ispatialaudioclient_isaudioobjectformatsupported","spatialaudioclient/ISpatialAudioClient::IsAudioObjectFormatSupported"]
old-location: coreaudio\ispatialaudioclient_isaudioobjectformatsupported.htm
tech.root: CoreAudio
ms.assetid: 47AB0B3B-E8D0-412F-AC9C-F8BC700E7C23
ms.date: 12/05/2018
ms.keywords: ISpatialAudioClient interface [Core Audio],IsAudioObjectFormatSupported method, ISpatialAudioClient.IsAudioObjectFormatSupported, ISpatialAudioClient::IsAudioObjectFormatSupported, IsAudioObjectFormatSupported, IsAudioObjectFormatSupported method [Core Audio], IsAudioObjectFormatSupported method [Core Audio],ISpatialAudioClient interface, coreaudio.ispatialaudioclient_isaudioobjectformatsupported, spatialaudioclient/ISpatialAudioClient::IsAudioObjectFormatSupported
req.header: spatialaudioclient.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioClient::IsAudioObjectFormatSupported
 - spatialaudioclient/ISpatialAudioClient::IsAudioObjectFormatSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.IsAudioObjectFormatSupported
---

# ISpatialAudioClient::IsAudioObjectFormatSupported


## -description

Gets a value indicating whether <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a> supports a the specified format.

## -parameters

### -param objectFormat [in]

The format for which support is queried.

## -returns

If the specified format is supported, it returns S_OK. If specified format is unsupported, this method returns AUDCLNT_E_UNSUPPORTED_FORMAT.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>