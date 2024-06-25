---
UID: NF:strmif.IAMVideoProcAmp.Set
title: IAMVideoProcAmp::Set (strmif.h)
description: The Set method sets video quality for a specified property.
helpviewer_keywords: ["IAMVideoProcAmp interface [DirectShow]","Set method","IAMVideoProcAmp.Set","IAMVideoProcAmp::Set","IAMVideoProcAmpSet","Set","Set method [DirectShow]","Set method [DirectShow]","IAMVideoProcAmp interface","dshow.iamvideoprocamp_set","strmif/IAMVideoProcAmp::Set"]
old-location: dshow\iamvideoprocamp_set.htm
tech.root: dshow
ms.assetid: 18826377-ddf7-4c36-8995-43310ea077dd
ms.date: 4/26/2023
ms.keywords: IAMVideoProcAmp interface [DirectShow],Set method, IAMVideoProcAmp.Set, IAMVideoProcAmp::Set, IAMVideoProcAmpSet, Set, Set method [DirectShow], Set method [DirectShow],IAMVideoProcAmp interface, dshow.iamvideoprocamp_set, strmif/IAMVideoProcAmp::Set
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVideoProcAmp::Set
 - strmif/IAMVideoProcAmp::Set
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoProcAmp.Set
---

# IAMVideoProcAmp::Set


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Set</b> method sets video quality for a specified property.

## -parameters

### -param Property [in]

The property to set, specified as a [VideoProcAmpProperty](/windows/desktop/api/strmif/ne-strmif-videoprocampproperty) enumeration value.

### -param lValue [in]

The new value of the property.

### -param Flags [in]

The desired control setting, specified as a [VideoProcAmpFlags](/windows/desktop/api/strmif/ne-strmif-videoprocampflags) enumeration
          value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>Flags</i> parameter is <b>VideoProcAmp_Flags_Auto</b>, the <i>lValue</i> parameter is ignored, as long as it's between the minimum and maximum values of the property.

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-get">IAMVideoProcAmp::Get</a>
