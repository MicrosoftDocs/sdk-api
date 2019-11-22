---
UID: NF:mfmediaengine.IMFMediaEngine.SetAutoPlay
title: IMFMediaEngine::SetAutoPlay (mfmediaengine.h)

description: Specifies whether the Media Engine automatically begins playback.
old-location: mf\imfmediaengine_setautoplay.htm
tech.root: medfound
ms.assetid: 867FE1D2-39AE-4A44-99DD-98A8ABD234A2

ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetAutoPlay method, IMFMediaEngine.SetAutoPlay, IMFMediaEngine::SetAutoPlay, SetAutoPlay, SetAutoPlay method [Media Foundation], SetAutoPlay method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setautoplay, mfmediaengine/IMFMediaEngine::SetAutoPlay
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngine.SetAutoPlay"
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
 - IMFMediaEngine.SetAutoPlay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::SetAutoPlay


## -description


Specifies whether the Media Engine automatically begins playback.


## -parameters




### -param AutoPlay [in]

If <b>TRUE</b>, the Media Engine automatically begins playback after it loads a media source. Otherwise, playback does not begin until the application calls <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

