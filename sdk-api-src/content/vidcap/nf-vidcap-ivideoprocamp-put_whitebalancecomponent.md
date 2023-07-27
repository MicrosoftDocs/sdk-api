---
UID: NF:vidcap.IVideoProcAmp.put_WhiteBalanceComponent
title: IVideoProcAmp::put_WhiteBalanceComponent (vidcap.h)
description: The put_WhiteBalanceComponent method sets the camera's white balance, specified as red and blue component values.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_WhiteBalanceComponent method","IVideoProcAmp.put_WhiteBalanceComponent","IVideoProcAmp::put_WhiteBalanceComponent","IVideoProcAmpput_WhiteBalanceComponent","dshow.ivideoprocamp_put_whitebalancecomponent","put_WhiteBalanceComponent","put_WhiteBalanceComponent method [DirectShow]","put_WhiteBalanceComponent method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_WhiteBalanceComponent"]
old-location: dshow\ivideoprocamp_put_whitebalancecomponent.htm
tech.root: dshow
ms.assetid: 800d7ddb-9f66-4fc4-a246-e6501377b9ce
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],put_WhiteBalanceComponent method, IVideoProcAmp.put_WhiteBalanceComponent, IVideoProcAmp::put_WhiteBalanceComponent, IVideoProcAmpput_WhiteBalanceComponent, dshow.ivideoprocamp_put_whitebalancecomponent, put_WhiteBalanceComponent, put_WhiteBalanceComponent method [DirectShow], put_WhiteBalanceComponent method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_WhiteBalanceComponent
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVideoProcAmp::put_WhiteBalanceComponent
 - vidcap/IVideoProcAmp::put_WhiteBalanceComponent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.put_WhiteBalanceComponent
---

# IVideoProcAmp::put_WhiteBalanceComponent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_WhiteBalanceComponent</code> method sets the camera's white balance, specified as red and blue component values.

## -parameters

### -param Value1 [in]

Specifies the red component.

### -param Value2 [in]

Specifies the blue component.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>