---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetAudioStreamCategory
title: IMFMediaEngineEx::GetAudioStreamCategory (mfmediaengine.h)
author: windows-sdk-content
description: Gets the audio stream category used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_getaudiostreamcategory.htm
tech.root: medfound
ms.assetid: 587c0844-93be-42e4-96f6-d5aa721e9ced
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAudioStreamCategory, GetAudioStreamCategory method [Media Foundation], GetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetAudioStreamCategory method, IMFMediaEngineEx.GetAudioStreamCategory, IMFMediaEngineEx::GetAudioStreamCategory, mf.imfmediaengineex_getaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::GetAudioStreamCategory
ms.topic: method
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
 - IMFMediaEngineEx.GetAudioStreamCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::GetAudioStreamCategory


## -description


Gets the audio stream category used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 


## -parameters




### -param pCategory [out]

Receives the audio stream category.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio stream categories, see <a href="https://docs.microsoft.com/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-_audio_stream_category">AUDIO_STREAM_CATEGORY enumeration</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

