---
UID: NF:strmif.IAMVideoDecimationProperties.QueryDecimationUsage
title: IAMVideoDecimationProperties::QueryDecimationUsage (strmif.h)
description: The QueryDecimationUsage method retrieves the current decimation strategy.
helpviewer_keywords: ["IAMVideoDecimationProperties interface [DirectShow]","QueryDecimationUsage method","IAMVideoDecimationProperties.QueryDecimationUsage","IAMVideoDecimationProperties::QueryDecimationUsage","IAMVideoDecimationPropertiesQueryDecimationUsage","QueryDecimationUsage","QueryDecimationUsage method [DirectShow]","QueryDecimationUsage method [DirectShow]","IAMVideoDecimationProperties interface","dshow.iamvideodecimationproperties_querydecimationusage","strmif/IAMVideoDecimationProperties::QueryDecimationUsage"]
old-location: dshow\iamvideodecimationproperties_querydecimationusage.htm
tech.root: dshow
ms.assetid: 3addb9be-61df-4310-9066-85f75c64aae4
ms.date: 4/26/2023
ms.keywords: IAMVideoDecimationProperties interface [DirectShow],QueryDecimationUsage method, IAMVideoDecimationProperties.QueryDecimationUsage, IAMVideoDecimationProperties::QueryDecimationUsage, IAMVideoDecimationPropertiesQueryDecimationUsage, QueryDecimationUsage, QueryDecimationUsage method [DirectShow], QueryDecimationUsage method [DirectShow],IAMVideoDecimationProperties interface, dshow.iamvideodecimationproperties_querydecimationusage, strmif/IAMVideoDecimationProperties::QueryDecimationUsage
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
 - IAMVideoDecimationProperties::QueryDecimationUsage
 - strmif/IAMVideoDecimationProperties::QueryDecimationUsage
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
 - IAMVideoDecimationProperties.QueryDecimationUsage
---

# IAMVideoDecimationProperties::QueryDecimationUsage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryDecimationUsage</code> method retrieves the current decimation strategy.

## -parameters

### -param lpUsage [out]

Pointer to a variable of type [DECIMATION_USAGE](/windows/desktop/api/strmif/ne-strmif-decimation_usage) that receives the decimation setting.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_FAIL or another error code otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideodecimationproperties">IAMVideoDecimationProperties Interface</a>