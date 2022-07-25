---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetAudioStreamCategory
title: IMFMediaEngineEx::GetAudioStreamCategory (mfmediaengine.h)
description: Gets the audio stream category used for the next call to SetSource or Load.
helpviewer_keywords: ["GetAudioStreamCategory","GetAudioStreamCategory method [Media Foundation]","GetAudioStreamCategory method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetAudioStreamCategory method","IMFMediaEngineEx.GetAudioStreamCategory","IMFMediaEngineEx::GetAudioStreamCategory","mf.imfmediaengineex_getaudiostreamcategory","mfmediaengine/IMFMediaEngineEx::GetAudioStreamCategory"]
old-location: mf\imfmediaengineex_getaudiostreamcategory.htm
tech.root: mf
ms.assetid: 587c0844-93be-42e4-96f6-d5aa721e9ced
ms.date: 12/05/2018
ms.keywords: GetAudioStreamCategory, GetAudioStreamCategory method [Media Foundation], GetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetAudioStreamCategory method, IMFMediaEngineEx.GetAudioStreamCategory, IMFMediaEngineEx::GetAudioStreamCategory, mf.imfmediaengineex_getaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::GetAudioStreamCategory
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::GetAudioStreamCategory
 - mfmediaengine/IMFMediaEngineEx::GetAudioStreamCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetAudioStreamCategory
---

# IMFMediaEngineEx::GetAudioStreamCategory


## -description

Gets the audio stream category used for the next call to <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param pCategory [out]

Receives the audio stream category.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information on audio stream categories, see <a href="/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category">AUDIO_STREAM_CATEGORY enumeration</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>