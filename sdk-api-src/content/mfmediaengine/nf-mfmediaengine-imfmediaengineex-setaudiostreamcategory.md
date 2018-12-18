---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioStreamCategory
title: IMFMediaEngineEx::SetAudioStreamCategory
author: windows-sdk-content
description: Sets the audio stream category for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_setaudiostreamcategory.htm
tech.root: medfound
ms.assetid: 55906e89-4064-4355-ad44-7d7d973ddb2c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioStreamCategory method, IMFMediaEngineEx.SetAudioStreamCategory, IMFMediaEngineEx::SetAudioStreamCategory, SetAudioStreamCategory, SetAudioStreamCategory method [Media Foundation], SetAudioStreamCategory method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudiostreamcategory, mfmediaengine/IMFMediaEngineEx::SetAudioStreamCategory
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
 - IMFMediaEngineEx.SetAudioStreamCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::SetAudioStreamCategory


## -description


Sets the audio stream category for the next call to  <a href="https://msdn.microsoft.com/80C41EAB-9B8F-4723-A4A7-A17F56FF5773">SetSource</a> or <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a>. 


## -parameters




### -param category [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio stream categories, see <a href="https://msdn.microsoft.com/B6B9195A-2704-4633-AFCF-B01CED6B6DB4">AUDIO_STREAM_CATEGORY enumeration</a>.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

