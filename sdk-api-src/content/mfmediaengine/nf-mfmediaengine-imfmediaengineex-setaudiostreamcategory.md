---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioStreamCategory
title: IMFMediaEngineEx::SetAudioStreamCategory (mfmediaengine.h)
description: Sets the audio stream category for the next call to SetSource or Load.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetAudioStreamCategory method","IMFMediaEngineEx.SetAudioStreamCategory","IMFMediaEngineEx::SetAudioStreamCategory","SetAudioStreamCategory","SetAudioStreamCategory method [Media Foundation]","SetAudioStreamCategory method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setaudiostreamcategory","mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory"]
old-location: mf\imfmediaengineex_setaudiostreamcategory.htm
tech.root: medfound
ms.assetid: 55906e89-4064-4355-ad44-7d7d973ddb2c
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioStreamCategory method, IMFMediaEngineEx.SetAudioStreamCategory, IMFMediaEngineEx::SetAudioStreamCategory, SetAudioStreamCategory, SetAudioStreamCategory method [Media Foundation], SetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory
f1_keywords:
- mfmediaengine/IMFMediaEngineEx.SetAudioStreamCategory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFMediaEngineEx.SetAudioStreamCategory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::SetAudioStreamCategory


## -description


Sets the audio stream category for the next call to  <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 


## -parameters




### -param category [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio stream categories, see <a href="https://docs.microsoft.com/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category">AUDIO_STREAM_CATEGORY enumeration</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

