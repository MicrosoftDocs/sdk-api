---
UID: NF:videoacc.IAMVideoAccelerator.GetVideoAcceleratorGUIDs
title: IAMVideoAccelerator::GetVideoAcceleratorGUIDs (videoacc.h)
description: The GetVideoAcceleratorGUIDs method gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.
helpviewer_keywords: ["GetVideoAcceleratorGUIDs","GetVideoAcceleratorGUIDs method [DirectShow]","GetVideoAcceleratorGUIDs method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","GetVideoAcceleratorGUIDs method","IAMVideoAccelerator.GetVideoAcceleratorGUIDs","IAMVideoAccelerator::GetVideoAcceleratorGUIDs","IAMVideoAcceleratorGetVideoAcceleratorGUIDs","dshow.iamvideoaccelerator_getvideoacceleratorguids","videoacc/IAMVideoAccelerator::GetVideoAcceleratorGUIDs"]
old-location: dshow\iamvideoaccelerator_getvideoacceleratorguids.htm
tech.root: dshow
ms.assetid: 808ba120-f0e1-4348-94e7-69a27c77cf42
ms.date: 4/26/2023
ms.keywords: GetVideoAcceleratorGUIDs, GetVideoAcceleratorGUIDs method [DirectShow], GetVideoAcceleratorGUIDs method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetVideoAcceleratorGUIDs method, IAMVideoAccelerator.GetVideoAcceleratorGUIDs, IAMVideoAccelerator::GetVideoAcceleratorGUIDs, IAMVideoAcceleratorGetVideoAcceleratorGUIDs, dshow.iamvideoaccelerator_getvideoacceleratorguids, videoacc/IAMVideoAccelerator::GetVideoAcceleratorGUIDs
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
 - IAMVideoAccelerator::GetVideoAcceleratorGUIDs
 - videoacc/IAMVideoAccelerator::GetVideoAcceleratorGUIDs
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
 - IAMVideoAccelerator.GetVideoAcceleratorGUIDs
---

# IAMVideoAccelerator::GetVideoAcceleratorGUIDs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetVideoAcceleratorGUIDs</b> method gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.

## -parameters

### -param pdwNumGuidsSupported [in, out]

On input, specifies the number of elements in the <i>pGuidsSupported</i> array.
            If <i>pGuidsSupported</i> is <b>NULL</b>, the value of <code>*pdwNumGuidsSupported</code> must be zero. 

On output, if <i>pGuidsSupported</i> is <b>NULL</b>, <i>pdwNumGuidsSupported</i> receives the number of restricted-mode DXVA profiles. Otherwise, <i>pdwNumGuidsSupported</i> receives the actual number of GUIDs copied to the <i>pGuidsSupported</i> array.

### -param pGuidsSupported [in, out]

Address of an array of GUIDs, or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of GUIDs that specify restricted-mode DXVA profiles. These GUIDs are defined in the header file dxva.h, and are documented in the <a href="/windows-hardware/drivers/display/directx-video-acceleration">DXVA 1.0 specification</a>.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Invalid state. The video renderer has not created the Direct3D or DirectDraw device.

</td>
</tr>
</table>

## -remarks

Call this method twice. On the first call, set <i>pGuidsSupported</i> to <b>NULL</b>. The <i>pdwNumGuidsSupported</i> parameter receives the number of DXVA profile GUIDs. Allocate an array of GUIDs with the required size and call the method again. This time, set <i>pGuidsSupported</i> to the address of the array. The method fills the array with the list of DXVA profile GUIDs.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>