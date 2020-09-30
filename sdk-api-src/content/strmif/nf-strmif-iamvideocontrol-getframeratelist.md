---
UID: NF:strmif.IAMVideoControl.GetFrameRateList
title: IAMVideoControl::GetFrameRateList (strmif.h)
description: The GetFrameRateList method retrieves a list of available frame rates.
helpviewer_keywords: ["GetFrameRateList","GetFrameRateList method [DirectShow]","GetFrameRateList method [DirectShow]","IAMVideoControl interface","IAMVideoControl interface [DirectShow]","GetFrameRateList method","IAMVideoControl.GetFrameRateList","IAMVideoControl::GetFrameRateList","IAMVideoControlGetFrameRateList","dshow.iamvideocontrol_getframeratelist","strmif/IAMVideoControl::GetFrameRateList"]
old-location: dshow\iamvideocontrol_getframeratelist.htm
tech.root: dshow
ms.assetid: 864f294f-1a18-4d4c-952e-1965da4c9496
ms.date: 12/05/2018
ms.keywords: GetFrameRateList, GetFrameRateList method [DirectShow], GetFrameRateList method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetFrameRateList method, IAMVideoControl.GetFrameRateList, IAMVideoControl::GetFrameRateList, IAMVideoControlGetFrameRateList, dshow.iamvideocontrol_getframeratelist, strmif/IAMVideoControl::GetFrameRateList
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
 - IAMVideoControl::GetFrameRateList
 - strmif/IAMVideoControl::GetFrameRateList
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
 - IAMVideoControl.GetFrameRateList
---

# IAMVideoControl::GetFrameRateList


## -description

The <code>GetFrameRateList</code> method retrieves a list of available frame rates.

## -parameters

### -param pPin [in]

Pointer to the pin to query for the list of frame rates.

### -param iIndex [in]

Index of the format to query for frame rates. This index corresponds to the order in which formats are enumerated by [VIDEO_STREAM_CONFIG_CAPS](/windows/desktop/api/strmif/ns-strmif-video_stream_config_caps) structures returned by <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities">IAMStreamConfig::GetNumberOfCapabilities</a>) minus one.

### -param Dimensions [in]

Frame image size (width and height) in pixels.

### -param ListSize [out]

Pointer to the number of elements in the list of frame rates.

### -param FrameRates [out]

Address of a pointer to an array of frame rates in 100-nanosecond units. Can be <b>NULL</b> if you only need <i>ListSize</i>.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

The caller is responsible for freeing the memory through a call to <b>CoTaskMemFree</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>



[VIDEO_STREAM_CONFIG_CAPS Structure](/windows/desktop/api/strmif/ns-strmif-video_stream_config_caps)