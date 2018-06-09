---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetAudioStreamCategory
title: IMFMediaEngineEx::GetAudioStreamCategory
author: windows-sdk-content
description: Gets the audio stream category used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_getaudiostreamcategory.htm
old-project: medfound
ms.assetid: 587c0844-93be-42e4-96f6-d5aa721e9ced
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetAudioStreamCategory, GetAudioStreamCategory method [Media Foundation], GetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetAudioStreamCategory method, IMFMediaEngineEx.GetAudioStreamCategory, IMFMediaEngineEx::GetAudioStreamCategory, mf.imfmediaengineex_getaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::GetAudioStreamCategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MF_MEDIA_ENGINE_KEYERR
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::GetAudioStreamCategory


## -description


Gets the audio stream category used for the next call to <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 


## -parameters




### -param pCategory [out]

Receives the audio stream category.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio stream categories, see <a href="https://msdn.microsoft.com/B6B9195A-2704-4633-AFCF-B01CED6B6DB4">AUDIO_STREAM_CATEGORY enumeration</a>.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

