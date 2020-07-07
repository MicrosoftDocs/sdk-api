---
UID: NF:mfmediaengine.IMFMediaEngine.SetPlaybackRate
title: IMFMediaEngine::SetPlaybackRate (mfmediaengine.h)
description: Sets the current playback rate.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetPlaybackRate method","IMFMediaEngine.SetPlaybackRate","IMFMediaEngine::SetPlaybackRate","SetPlaybackRate","SetPlaybackRate method [Media Foundation]","SetPlaybackRate method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setplaybackrate","mfmediaengine/IMFMediaEngine::SetPlaybackRate"]
old-location: mf\imfmediaengine_setplaybackrate.htm
tech.root: medfound
ms.assetid: 648BF1CC-BFAC-4874-808B-F8B46E3E9989
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetPlaybackRate method, IMFMediaEngine.SetPlaybackRate, IMFMediaEngine::SetPlaybackRate, SetPlaybackRate, SetPlaybackRate method [Media Foundation], SetPlaybackRate method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setplaybackrate, mfmediaengine/IMFMediaEngine::SetPlaybackRate
f1_keywords:
- mfmediaengine/IMFMediaEngine.SetPlaybackRate
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
- IMFMediaEngine.SetPlaybackRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::SetPlaybackRate


## -description


Sets the current playback rate.


## -parameters




### -param Rate [in]

The playback rate, as a multiple of normal (1×) playback. A negative value indicates reverse playback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>playbackRate</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

