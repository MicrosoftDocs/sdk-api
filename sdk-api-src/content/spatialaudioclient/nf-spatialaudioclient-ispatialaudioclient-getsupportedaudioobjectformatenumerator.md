---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetSupportedAudioObjectFormatEnumerator
title: ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator (spatialaudioclient.h)
description: Gets an IAudioFormatEnumerator that contains all supported audio formats for spatial audio objects, the first item in the list represents the most preferable format.
helpviewer_keywords: ["GetSupportedAudioObjectFormatEnumerator","GetSupportedAudioObjectFormatEnumerator method [Core Audio]","GetSupportedAudioObjectFormatEnumerator method [Core Audio]","ISpatialAudioClient interface","ISpatialAudioClient interface [Core Audio]","GetSupportedAudioObjectFormatEnumerator method","ISpatialAudioClient.GetSupportedAudioObjectFormatEnumerator","ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator","coreaudio.ispatialaudioclient_getsupportedaudioobjectformatenumerator","spatialaudioclient/ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator"]
old-location: coreaudio\ispatialaudioclient_getsupportedaudioobjectformatenumerator.htm
tech.root: CoreAudio
ms.assetid: CB152D8C-DE3A-4224-A6CC-DF1BFF1A3ABA
ms.date: 12/05/2018
ms.keywords: GetSupportedAudioObjectFormatEnumerator, GetSupportedAudioObjectFormatEnumerator method [Core Audio], GetSupportedAudioObjectFormatEnumerator method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetSupportedAudioObjectFormatEnumerator method, ISpatialAudioClient.GetSupportedAudioObjectFormatEnumerator, ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator, coreaudio.ispatialaudioclient_getsupportedaudioobjectformatenumerator, spatialaudioclient/ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator
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
 - ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator
 - spatialaudioclient/ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator
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
 - ISpatialAudioClient.GetSupportedAudioObjectFormatEnumerator
---

# ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator


## -description

Gets an <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-iaudioformatenumerator">IAudioFormatEnumerator</a> that contains  all supported audio formats for spatial audio objects, the first item in the list represents the most preferable format.

## -parameters

### -param enumerator [out]

Pointer to the pointer that receives the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-iaudioformatenumerator">IAudioFormatEnumerator</a> interface.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>