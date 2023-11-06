---
UID: NF:strmif.IAMVideoDecimationProperties.SetDecimationUsage
title: IAMVideoDecimationProperties::SetDecimationUsage (strmif.h)
description: The SetDecimationUsage method sets the decimation strategy.
helpviewer_keywords: ["IAMVideoDecimationProperties interface [DirectShow]","SetDecimationUsage method","IAMVideoDecimationProperties.SetDecimationUsage","IAMVideoDecimationProperties::SetDecimationUsage","IAMVideoDecimationPropertiesSetDecimationUsage","SetDecimationUsage","SetDecimationUsage method [DirectShow]","SetDecimationUsage method [DirectShow]","IAMVideoDecimationProperties interface","dshow.iamvideodecimationproperties_setdecimationusage","strmif/IAMVideoDecimationProperties::SetDecimationUsage"]
old-location: dshow\iamvideodecimationproperties_setdecimationusage.htm
tech.root: dshow
ms.assetid: c6456154-48f5-41d9-b6f5-863b30a53596
ms.date: 4/26/2023
ms.keywords: IAMVideoDecimationProperties interface [DirectShow],SetDecimationUsage method, IAMVideoDecimationProperties.SetDecimationUsage, IAMVideoDecimationProperties::SetDecimationUsage, IAMVideoDecimationPropertiesSetDecimationUsage, SetDecimationUsage, SetDecimationUsage method [DirectShow], SetDecimationUsage method [DirectShow],IAMVideoDecimationProperties interface, dshow.iamvideodecimationproperties_setdecimationusage, strmif/IAMVideoDecimationProperties::SetDecimationUsage
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMVideoDecimationProperties::SetDecimationUsage
 - strmif/IAMVideoDecimationProperties::SetDecimationUsage
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
 - IAMVideoDecimationProperties.SetDecimationUsage
---

# IAMVideoDecimationProperties::SetDecimationUsage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDecimationUsage</code> method sets the decimation strategy.

## -parameters

### -param Usage [in]

Member of the [DECIMATION_USAGE](/windows/desktop/api/strmif/ne-strmif-decimation_usage) enumeration that specifies the decimation strategy.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_INVALIDARG otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideodecimationproperties">IAMVideoDecimationProperties Interface</a>