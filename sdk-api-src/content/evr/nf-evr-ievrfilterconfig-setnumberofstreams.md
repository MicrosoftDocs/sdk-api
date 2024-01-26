---
UID: NF:evr.IEVRFilterConfig.SetNumberOfStreams
title: IEVRFilterConfig::SetNumberOfStreams (evr.h)
description: Sets the number of input pins on the EVR filter.
helpviewer_keywords: ["72777c3d-b098-43b9-80ea-ef180b7f1a4a","IEVRFilterConfig interface [Media Foundation]","SetNumberOfStreams method","IEVRFilterConfig.SetNumberOfStreams","IEVRFilterConfig::SetNumberOfStreams","SetNumberOfStreams","SetNumberOfStreams method [Media Foundation]","SetNumberOfStreams method [Media Foundation]","IEVRFilterConfig interface","evr/IEVRFilterConfig::SetNumberOfStreams","mf.ievrfilterconfig_setnumberofstreams"]
old-location: mf\ievrfilterconfig_setnumberofstreams.htm
tech.root: mfarchive
ms.assetid: 72777c3d-b098-43b9-80ea-ef180b7f1a4a
ms.date: 12/05/2018
ms.keywords: 72777c3d-b098-43b9-80ea-ef180b7f1a4a, IEVRFilterConfig interface [Media Foundation],SetNumberOfStreams method, IEVRFilterConfig.SetNumberOfStreams, IEVRFilterConfig::SetNumberOfStreams, SetNumberOfStreams, SetNumberOfStreams method [Media Foundation], SetNumberOfStreams method [Media Foundation],IEVRFilterConfig interface, evr/IEVRFilterConfig::SetNumberOfStreams, mf.ievrfilterconfig_setnumberofstreams
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IEVRFilterConfig::SetNumberOfStreams
 - evr/IEVRFilterConfig::SetNumberOfStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRFilterConfig.SetNumberOfStreams
archived: true
---

# IEVRFilterConfig::SetNumberOfStreams


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the number of input pins on the EVR filter.

## -parameters

### -param dwMaxStreams [in]

Specifies the total number of input pins on the EVR filter. This value includes the input pin for the reference stream, which is created by default. For example, to mix one substream plus the reference stream, set this parameter to 2.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid number of streams. The minimum is one, and the maximum is 16.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
This method has already been called, or at least one pin is already connected.

</td>
</tr>
</table>

## -remarks

After this method has been called, it cannot be called a second time on the same instance of the EVR filter. Also, the method fails if any input pins are connected.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>