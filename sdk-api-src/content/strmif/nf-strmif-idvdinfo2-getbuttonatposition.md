---
UID: NF:strmif.IDvdInfo2.GetButtonAtPosition
title: IDvdInfo2::GetButtonAtPosition (strmif.h)
description: The GetButtonAtPosition method retrieves the button located at the specified point within the display window.
helpviewer_keywords: ["GetButtonAtPosition","GetButtonAtPosition method [DirectShow]","GetButtonAtPosition method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetButtonAtPosition method","IDvdInfo2.GetButtonAtPosition","IDvdInfo2::GetButtonAtPosition","IDvdInfo2GetButtonAtPosition","dshow.idvdinfo2_getbuttonatposition","strmif/IDvdInfo2::GetButtonAtPosition"]
old-location: dshow\idvdinfo2_getbuttonatposition.htm
tech.root: dshow
ms.assetid: f9c506b3-c9d9-4dc2-b318-f987ab8636dc
ms.date: 4/26/2023
ms.keywords: GetButtonAtPosition, GetButtonAtPosition method [DirectShow], GetButtonAtPosition method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetButtonAtPosition method, IDvdInfo2.GetButtonAtPosition, IDvdInfo2::GetButtonAtPosition, IDvdInfo2GetButtonAtPosition, dshow.idvdinfo2_getbuttonatposition, strmif/IDvdInfo2::GetButtonAtPosition
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDvdInfo2::GetButtonAtPosition
 - strmif/IDvdInfo2::GetButtonAtPosition
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
 - IDvdInfo2.GetButtonAtPosition
---

# IDvdInfo2::GetButtonAtPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetButtonAtPosition</code> method retrieves the button located at the specified point within the display window.

## -parameters

### -param point [in]

Current mouse pointer position as retrieved through the Win32 WM_MOUSEMOVE message.

### -param pulButtonIndex [out]

Receives the index (from 1 through 36) of the button at the current mouse pointer position.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>puButtonIndex</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button at <i>point</i>.

</td>
</tr>
</table>

## -remarks

This method is typically called in response to a mouse pointer move within a DVD menu display window. Be sure to check for success in the <b>HRESULT</b> before trying to retrieve the button number; this method only sets the value of <i>puButtonIndex</i> if a button is found at the specified point. DVD buttons do not necessarily have highlighted rectangles, button rectangles can overlap, and button rectangles do not always correspond to the visual representation of the buttons.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>