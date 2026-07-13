---
UID: NF:videoacc.IAMVideoAccelerator.GetUncompFormatsSupported
title: IAMVideoAccelerator::GetUncompFormatsSupported (videoacc.h)
description: The GetUncompFormatsSupported method gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.
helpviewer_keywords: ["GetUncompFormatsSupported","GetUncompFormatsSupported method [DirectShow]","GetUncompFormatsSupported method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","GetUncompFormatsSupported method","IAMVideoAccelerator.GetUncompFormatsSupported","IAMVideoAccelerator::GetUncompFormatsSupported","IAMVideoAcceleratorGetUncompFormatsSupported","dshow.iamvideoaccelerator_getuncompformatssupported","videoacc/IAMVideoAccelerator::GetUncompFormatsSupported"]
old-location: dshow\iamvideoaccelerator_getuncompformatssupported.htm
tech.root: dshow
ms.assetid: 33f9a4ee-4de9-4853-9581-808d7a07bfc4
ms.date: 4/26/2023
ms.keywords: GetUncompFormatsSupported, GetUncompFormatsSupported method [DirectShow], GetUncompFormatsSupported method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetUncompFormatsSupported method, IAMVideoAccelerator.GetUncompFormatsSupported, IAMVideoAccelerator::GetUncompFormatsSupported, IAMVideoAcceleratorGetUncompFormatsSupported, dshow.iamvideoaccelerator_getuncompformatssupported, videoacc/IAMVideoAccelerator::GetUncompFormatsSupported
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
 - IAMVideoAccelerator::GetUncompFormatsSupported
 - videoacc/IAMVideoAccelerator::GetUncompFormatsSupported
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
 - IAMVideoAccelerator.GetUncompFormatsSupported
---

# IAMVideoAccelerator::GetUncompFormatsSupported


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetUncompFormatsSupported</b> method gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.

## -parameters

### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile. To get a list of supported profiles, call 
          <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids">IAMVideoAccelerator::GetVideoAcceleratorGUIDs</a>.

### -param pdwNumFormatsSupported [in, out]

On input, specifies the number of elements in the <i>pFormatsSupported</i> array.
            If <i>pFormatsSupported</i> is <b>NULL</b>, the value of <code>*pdwNumFormatsSupported</code> must be zero.

On output, if <i>pFormatsSupported</i> is <b>NULL</b>, <i>pdwNumFormatsSupported</i> receives the number of supported pixel formats. Otherwise, <i>pdwNumFormatsSupported</i> receives the actual number of pixel formats copied to the <i>pFormatsSupported</i> array.

### -param pFormatsSupported [in, out]

Address of an array of <b>DDPIXELFORMAT</b> structures, or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of pixel formats.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
The method returned fewer formats than the total number that are supported, because the array was too small. Although this value is a failure code, you can ignore the error if you intentionally allocated a smaller array.

</td>
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
</table>

## -remarks

Call this method twice. On the first call, set <i>pFormatsSupported</i> to <b>NULL</b>. The <i>pdwNumFormatsSupported</i> parameter receives the number of formats. Allocate an array of <b>DDPIXELFORMAT</b> structures with the required size, and call the method again. This time, set <i>pFormatsSupported</i> to the address of the array. The method fills the array with the list of pixel formats.

The driver should return the formats in decreasing order of preference, with the most preferred format listed first.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>