---
UID: NF:vmr9.IVMRFilterConfig9.SetNumberOfStreams
title: IVMRFilterConfig9::SetNumberOfStreams (vmr9.h)
description: The SetNumberOfStreams method sets the number of streams to be mixed and instructs the VMR to go into mixer mode.
helpviewer_keywords: ["IVMRFilterConfig9 interface [DirectShow]","SetNumberOfStreams method","IVMRFilterConfig9.SetNumberOfStreams","IVMRFilterConfig9::SetNumberOfStreams","IVMRFilterConfig9SetNumberOfStreams","SetNumberOfStreams","SetNumberOfStreams method [DirectShow]","SetNumberOfStreams method [DirectShow]","IVMRFilterConfig9 interface","dshow.ivmrfilterconfig9_setnumberofstreams","vmr9/IVMRFilterConfig9::SetNumberOfStreams"]
old-location: dshow\ivmrfilterconfig9_setnumberofstreams.htm
tech.root: dshow
ms.assetid: 062aac78-6d7d-4335-963a-bc2c2d339efb
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetNumberOfStreams method, IVMRFilterConfig9.SetNumberOfStreams, IVMRFilterConfig9::SetNumberOfStreams, IVMRFilterConfig9SetNumberOfStreams, SetNumberOfStreams, SetNumberOfStreams method [DirectShow], SetNumberOfStreams method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setnumberofstreams, vmr9/IVMRFilterConfig9::SetNumberOfStreams
req.header: vmr9.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRFilterConfig9::SetNumberOfStreams
 - vmr9/IVMRFilterConfig9::SetNumberOfStreams
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
 - IVMRFilterConfig9.SetNumberOfStreams
---

# IVMRFilterConfig9::SetNumberOfStreams


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetNumberOfStreams</code> method sets the number of streams to be mixed and instructs the VMR to go into mixer mode.

## -parameters

### -param dwMaxStreams [in]

Double word containing the maximum number of input streams that the VMR will be required to mix.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The mixer is already configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to configure the mixer for more than 16 input streams.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory to manage the streams could not be allocated.

</td>
</tr>
</table>

## -remarks

<i>dwMaxStreams</i> should be equal to the number of input pins required. Pins cannot be added or removed after the VMR has been connected. If you do not know in advance how many input streams will be required, set <i>dxMaxStreams</i> to the maximum number that might be required. A value of 1 is valid for dwMaxStreams. This value does not cause any extra pins to be created, but it does force the VMR to go into "mixer mode."

The VMR creates as many input pins as are specified without attempting to determine whether there is enough video memory to support them all. This is because it has no way of knowing the media type or rectangle dimensions at this time. Later, when an upstream filter attempts to connect to a pin, at that point the media type is known and the VMR will examine the video memory and fail the connection if there is not enough memory to process the stream.

<div class="alert"><b>Note</b>  Although the VMR supports multiple streams, they all share a single clock, and therefore you cannot seek one stream independently of the others. If you need to seek the input streams independently, you must use a different technique.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>