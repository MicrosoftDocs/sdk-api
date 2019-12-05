---
UID: NF:mfmediaengine.IMFMediaEngine.SetDefaultPlaybackRate
title: IMFMediaEngine::SetDefaultPlaybackRate (mfmediaengine.h)
description: Sets the default playback rate.
old-location: mf\imfmediaengine_setdefaultplaybackrate.htm
tech.root: medfound
ms.assetid: D6EA6BC1-021A-432D-BBCB-BE2FD15E7BE5
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetDefaultPlaybackRate method, IMFMediaEngine.SetDefaultPlaybackRate, IMFMediaEngine::SetDefaultPlaybackRate, SetDefaultPlaybackRate, SetDefaultPlaybackRate method [Media Foundation], SetDefaultPlaybackRate method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setdefaultplaybackrate, mfmediaengine/IMFMediaEngine::SetDefaultPlaybackRate
ms.topic: method
f1_keywords:
- mfmediaengine/IMFMediaEngine.SetDefaultPlaybackRate
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
- IMFMediaEngine.SetDefaultPlaybackRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::SetDefaultPlaybackRate


## -description


Sets the default playback rate.


## -parameters




### -param Rate [in]

The default playback rate, as a multiple of normal (1×) playback. A negative value indicates reverse playback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>defaultPlaybackRate</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

