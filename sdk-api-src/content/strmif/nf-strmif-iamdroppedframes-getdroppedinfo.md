---
UID: NF:strmif.IAMDroppedFrames.GetDroppedInfo
title: IAMDroppedFrames::GetDroppedInfo (strmif.h)
description: The GetDroppedInfo method retrieves an array of frame numbers that were dropped.
helpviewer_keywords: ["GetDroppedInfo","GetDroppedInfo method [DirectShow]","GetDroppedInfo method [DirectShow]","IAMDroppedFrames interface","IAMDroppedFrames interface [DirectShow]","GetDroppedInfo method","IAMDroppedFrames.GetDroppedInfo","IAMDroppedFrames::GetDroppedInfo","IAMDroppedFramesGetDroppedInfo","dshow.iamdroppedframes_getdroppedinfo","strmif/IAMDroppedFrames::GetDroppedInfo"]
old-location: dshow\iamdroppedframes_getdroppedinfo.htm
tech.root: dshow
ms.assetid: d4dc9e68-f814-4bb4-88ea-88eea32b2577
ms.date: 4/26/2023
ms.keywords: GetDroppedInfo, GetDroppedInfo method [DirectShow], GetDroppedInfo method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetDroppedInfo method, IAMDroppedFrames.GetDroppedInfo, IAMDroppedFrames::GetDroppedInfo, IAMDroppedFramesGetDroppedInfo, dshow.iamdroppedframes_getdroppedinfo, strmif/IAMDroppedFrames::GetDroppedInfo
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
 - IAMDroppedFrames::GetDroppedInfo
 - strmif/IAMDroppedFrames::GetDroppedInfo
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
 - IAMDroppedFrames.GetDroppedInfo
---

# IAMDroppedFrames::GetDroppedInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDroppedInfo</code> method retrieves an array of frame numbers that were dropped.

## -parameters

### -param lSize [in]

Specifies the size of the array.

### -param plArray [out]

Pointer to an array of size <i>lSize</i>, allocated by the caller. The method fills the array with the frame numbers of the first <i>lSize</i> frames that were dropped, up to a maximum number that is device-dependent.

### -param plNumCopied [out]

Pointer to a variable that receives the number of items returned in <i>plArray</i>. This number might be less than the value of <i>lSize</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; the <i>lSize</i> parameter must by greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Not supported by this device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdroppedframes">IAMDroppedFrames Interface</a>