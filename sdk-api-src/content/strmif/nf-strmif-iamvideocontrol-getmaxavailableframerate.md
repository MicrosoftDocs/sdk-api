---
UID: NF:strmif.IAMVideoControl.GetMaxAvailableFrameRate
title: IAMVideoControl::GetMaxAvailableFrameRate (strmif.h)
description: The GetMaxAvailableFrameRate method retrieves the maximum frame rate currently available, based on bus bandwidth usage for connections, such as USB and IEEE 1394, where the maximum frame rate may be limited by bandwidth availability.
helpviewer_keywords: ["GetMaxAvailableFrameRate","GetMaxAvailableFrameRate method [DirectShow]","GetMaxAvailableFrameRate method [DirectShow]","IAMVideoControl interface","IAMVideoControl interface [DirectShow]","GetMaxAvailableFrameRate method","IAMVideoControl.GetMaxAvailableFrameRate","IAMVideoControl::GetMaxAvailableFrameRate","IAMVideoControlGetMaxAvailableFrameRate","dshow.iamvideocontrol_getmaxavailableframerate","strmif/IAMVideoControl::GetMaxAvailableFrameRate"]
old-location: dshow\iamvideocontrol_getmaxavailableframerate.htm
tech.root: dshow
ms.assetid: a196cf6e-491c-4d01-abfe-831440e75058
ms.date: 12/05/2018
ms.keywords: GetMaxAvailableFrameRate, GetMaxAvailableFrameRate method [DirectShow], GetMaxAvailableFrameRate method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetMaxAvailableFrameRate method, IAMVideoControl.GetMaxAvailableFrameRate, IAMVideoControl::GetMaxAvailableFrameRate, IAMVideoControlGetMaxAvailableFrameRate, dshow.iamvideocontrol_getmaxavailableframerate, strmif/IAMVideoControl::GetMaxAvailableFrameRate
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
 - IAMVideoControl::GetMaxAvailableFrameRate
 - strmif/IAMVideoControl::GetMaxAvailableFrameRate
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
 - IAMVideoControl.GetMaxAvailableFrameRate
---

# IAMVideoControl::GetMaxAvailableFrameRate


## -description

The <code>GetMaxAvailableFrameRate</code> method retrieves the maximum frame rate currently available, based on bus bandwidth usage for connections, such as USB and IEEE 1394, where the maximum frame rate may be limited by bandwidth availability.

## -parameters

### -param pPin [in]

Pointer to the pin to retrieve the maximum frame rate from.

### -param iIndex [in]

Index of the format to query for maximum frame rate. This index corresponds to the order in which formats are enumerated by <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getstreamcaps">IAMStreamConfig::GetStreamCaps</a>. The value must range between zero and the number of supported <b>VIDEO_STREAM_CONFIG_CAPS</b> structures returned by <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities">IAMStreamConfig::GetNumberOfCapabilities</a>) minus one.

### -param Dimensions [in]

Frame image size (width and height) in pixels.

### -param MaxAvailableFrameRate [out]

Pointer to the maximum available frame rate. The frame rate is expressed as frame duration in 100-nanosecond units.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>



[VIDEO_STREAM_CONFIG_CAPS Structure](/windows/desktop/api/strmif/ns-strmif-video_stream_config_caps)