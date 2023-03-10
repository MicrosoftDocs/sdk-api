---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioStreamCategory
title: IMFMediaEngineEx::SetAudioStreamCategory (mfmediaengine.h)
description: Sets the audio stream category for the next call to SetSource or Load.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetAudioStreamCategory method","IMFMediaEngineEx.SetAudioStreamCategory","IMFMediaEngineEx::SetAudioStreamCategory","SetAudioStreamCategory","SetAudioStreamCategory method [Media Foundation]","SetAudioStreamCategory method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setaudiostreamcategory","mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory"]
old-location: mf\imfmediaengineex_setaudiostreamcategory.htm
tech.root: mf
ms.assetid: 55906e89-4064-4355-ad44-7d7d973ddb2c
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioStreamCategory method, IMFMediaEngineEx.SetAudioStreamCategory, IMFMediaEngineEx::SetAudioStreamCategory, SetAudioStreamCategory, SetAudioStreamCategory method [Media Foundation], SetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory
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
 - IMFMediaEngineEx::SetAudioStreamCategory
 - mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory
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
 - IMFMediaEngineEx.SetAudioStreamCategory
---

# IMFMediaEngineEx::SetAudioStreamCategory


## -description

Sets the audio stream category for the next call to  <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param category [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information on audio stream categories, see <a href="/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category">AUDIO_STREAM_CATEGORY enumeration</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>