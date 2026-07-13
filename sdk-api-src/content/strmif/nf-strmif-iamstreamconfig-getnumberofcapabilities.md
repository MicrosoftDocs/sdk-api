---
UID: NF:strmif.IAMStreamConfig.GetNumberOfCapabilities
title: IAMStreamConfig::GetNumberOfCapabilities (strmif.h)
description: The GetNumberOfCapabilities method retrieves the number of format capabilities that this pin supports.
helpviewer_keywords: ["GetNumberOfCapabilities","GetNumberOfCapabilities method [DirectShow]","GetNumberOfCapabilities method [DirectShow]","IAMStreamConfig interface","IAMStreamConfig interface [DirectShow]","GetNumberOfCapabilities method","IAMStreamConfig.GetNumberOfCapabilities","IAMStreamConfig::GetNumberOfCapabilities","IAMStreamConfigGetNumberOfCapabilities","dshow.iamstreamconfig_getnumberofcapabilities","strmif/IAMStreamConfig::GetNumberOfCapabilities"]
old-location: dshow\iamstreamconfig_getnumberofcapabilities.htm
tech.root: dshow
ms.assetid: 355b8c4c-6d07-4d31-8dc5-ddc5ec2bf1cd
ms.date: 4/26/2023
ms.keywords: GetNumberOfCapabilities, GetNumberOfCapabilities method [DirectShow], GetNumberOfCapabilities method [DirectShow],IAMStreamConfig interface, IAMStreamConfig interface [DirectShow],GetNumberOfCapabilities method, IAMStreamConfig.GetNumberOfCapabilities, IAMStreamConfig::GetNumberOfCapabilities, IAMStreamConfigGetNumberOfCapabilities, dshow.iamstreamconfig_getnumberofcapabilities, strmif/IAMStreamConfig::GetNumberOfCapabilities
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
 - IAMStreamConfig::GetNumberOfCapabilities
 - strmif/IAMStreamConfig::GetNumberOfCapabilities
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
 - IAMStreamConfig.GetNumberOfCapabilities
---

# IAMStreamConfig::GetNumberOfCapabilities


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNumberOfCapabilities</code> method retrieves the number of format capabilities that this pin supports.

## -parameters

### -param piCount [out]

Pointer to a variable that receives the number of format capabilities.

### -param piSize [out]

Pointer to a variable that receives the size of the configuration structure in bytes. See Remarks for more information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The input pin is not connected.

</td>
</tr>
</table>

## -remarks

An output pin can support more than one set of format capabilities. This method returns the total number of capabilities that the pin supports; the number is returned in the <i>piCount</i> parameter. To retrieve a particular set of capabilities, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getstreamcaps">IAMStreamConfig::GetStreamCaps</a> method. Format capabilities are indexed from zero, so the value returned in <i>piCount</i> is one more than the upper bound.

Depending on the pin's format type, the [VIDEO_STREAM_CONFIG_CAPS](/windows/desktop/api/strmif/ns-strmif-video_stream_config_caps) structure (for video) or an [AUDIO_STREAM_CONFIG_CAPS](/windows/desktop/api/strmif/ns-strmif-audio_stream_config_caps) structure (for audio). The <i>piSize</i> parameter receives the size of the structure, in bytes.

On some compression filters, this method fails if the filter's input pin is not connected.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamconfig">IAMStreamConfig Interface</a>