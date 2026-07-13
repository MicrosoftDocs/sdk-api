---
UID: NF:videoacc.IAMVideoAccelerator.QueryRenderStatus
title: IAMVideoAccelerator::QueryRenderStatus (videoacc.h)
description: The QueryRenderStatus method queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.
helpviewer_keywords: ["AMVA_QUERYRENDERSTATUSF_READ","IAMVideoAccelerator interface [DirectShow]","QueryRenderStatus method","IAMVideoAccelerator.QueryRenderStatus","IAMVideoAccelerator::QueryRenderStatus","IAMVideoAcceleratorQueryRenderStatus","QueryRenderStatus","QueryRenderStatus method [DirectShow]","QueryRenderStatus method [DirectShow]","IAMVideoAccelerator interface","Zero","dshow.iamvideoaccelerator_queryrenderstatus","videoacc/IAMVideoAccelerator::QueryRenderStatus"]
old-location: dshow\iamvideoaccelerator_queryrenderstatus.htm
tech.root: dshow
ms.assetid: 29d77bd5-2823-4e67-a69f-2898ad4c467c
ms.date: 4/26/2023
ms.keywords: AMVA_QUERYRENDERSTATUSF_READ, IAMVideoAccelerator interface [DirectShow],QueryRenderStatus method, IAMVideoAccelerator.QueryRenderStatus, IAMVideoAccelerator::QueryRenderStatus, IAMVideoAcceleratorQueryRenderStatus, QueryRenderStatus, QueryRenderStatus method [DirectShow], QueryRenderStatus method [DirectShow],IAMVideoAccelerator interface, Zero, dshow.iamvideoaccelerator_queryrenderstatus, videoacc/IAMVideoAccelerator::QueryRenderStatus
req.header: videoacc.h
req.include-header: 
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
 - IAMVideoAccelerator::QueryRenderStatus
 - videoacc/IAMVideoAccelerator::QueryRenderStatus
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
 - IAMVideoAccelerator.QueryRenderStatus
---

# IAMVideoAccelerator::QueryRenderStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>QueryRenderStatus</b> method queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.

## -parameters

### -param dwTypeIndex [in]

Specifies the type of surface to query: 

<ul>
<li>For a compressed surface, specify one of the DXVA surface types defined in dxva.h. </li>
<li>For an uncompressed output surface, set this parameter to 0xFFFFFFFF. </li>
</ul>

### -param dwBufferIndex [in]

The zero-based index of the surface, within the pool of surfaces that were allocated  for the specified surface type.

### -param dwFlags [in]

Specifies the type of query to perform.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for writing.

</td>
</tr>
<tr>
<td width="40%"><a id="AMVA_QUERYRENDERSTATUSF_READ"></a><a id="amva_queryrenderstatusf_read"></a><dl>
<dt><b>AMVA_QUERYRENDERSTATUSF_READ</b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for reading.

</td>
</tr>
</table>

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_INVALIDSUBTYPE</b></dt>
</dl>
</td>
<td width="60%">
The decoder did not use a DXVA decoding type when it connected to the video renderer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pins on the decoder and video renderer filters are not connected.

</td>
</tr>
</table>

## -remarks

If the filter's pins are not connected, the method returns <b>VFW_E_NOT_CONNECTED</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>