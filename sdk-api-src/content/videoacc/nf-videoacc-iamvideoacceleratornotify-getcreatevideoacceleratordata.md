---
UID: NF:videoacc.IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData
title: IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData (videoacc.h)
description: The GetCreateVideoAcceleratorData method gets information needed to create a video accelerator object.
helpviewer_keywords: ["GetCreateVideoAcceleratorData","GetCreateVideoAcceleratorData method [DirectShow]","GetCreateVideoAcceleratorData method [DirectShow]","IAMVideoAcceleratorNotify interface","IAMVideoAcceleratorNotify interface [DirectShow]","GetCreateVideoAcceleratorData method","IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData","IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData","IAMVideoAcceleratorNotifyGetCreateVideoAcceleratorData","dshow.iamvideoacceleratornotify_getcreatevideoacceleratordata","videoacc/IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData"]
old-location: dshow\iamvideoacceleratornotify_getcreatevideoacceleratordata.htm
tech.root: dshow
ms.assetid: 72e3331d-1e54-4ec7-9972-7e39eaf2707d
ms.date: 4/26/2023
ms.keywords: GetCreateVideoAcceleratorData, GetCreateVideoAcceleratorData method [DirectShow], GetCreateVideoAcceleratorData method [DirectShow],IAMVideoAcceleratorNotify interface, IAMVideoAcceleratorNotify interface [DirectShow],GetCreateVideoAcceleratorData method, IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData, IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData, IAMVideoAcceleratorNotifyGetCreateVideoAcceleratorData, dshow.iamvideoacceleratornotify_getcreatevideoacceleratordata, videoacc/IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData
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
 - IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData
 - videoacc/IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData
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
 - IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData
---

# IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCreateVideoAcceleratorData</b> method gets information needed to create a video accelerator object.

## -parameters

### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile in use.

### -param pdwSizeMiscData [out]

Receives the size of the data returned in <i>ppMiscData</i>, in bytes.

### -param ppMiscData [out]

Receives a pointer to a buffer that contains a <b>DXVA_ConnectMode</b> structure. The decoder must call <b>CoTaskMemAlloc</b> to allocate the memory for the structure. The caller must free the memory by calling <b>CoTaskMemFree</b>.

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
Method is not supported.

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify">IAMVideoAcceleratorNotify Interface</a>