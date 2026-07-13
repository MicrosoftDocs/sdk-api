---
UID: NF:strmif.IDvdInfo2.GetCurrentButton
title: IDvdInfo2::GetCurrentButton (strmif.h)
description: The GetCurrentButton method retrieves the number of available buttons and the number of the currently selected button.
helpviewer_keywords: ["GetCurrentButton","GetCurrentButton method [DirectShow]","GetCurrentButton method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentButton method","IDvdInfo2.GetCurrentButton","IDvdInfo2::GetCurrentButton","IDvdInfo2GetCurrentButton","dshow.idvdinfo2_getcurrentbutton","strmif/IDvdInfo2::GetCurrentButton"]
old-location: dshow\idvdinfo2_getcurrentbutton.htm
tech.root: dshow
ms.assetid: 9e8d8a0e-6db8-495b-b968-8a4e63435b99
ms.date: 4/26/2023
ms.keywords: GetCurrentButton, GetCurrentButton method [DirectShow], GetCurrentButton method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentButton method, IDvdInfo2.GetCurrentButton, IDvdInfo2::GetCurrentButton, IDvdInfo2GetCurrentButton, dshow.idvdinfo2_getcurrentbutton, strmif/IDvdInfo2::GetCurrentButton
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
 - IDvdInfo2::GetCurrentButton
 - strmif/IDvdInfo2::GetCurrentButton
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
 - IDvdInfo2.GetCurrentButton
---

# IDvdInfo2::GetCurrentButton


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentButton</code> method retrieves the number of available buttons and the number of the currently selected button.

## -parameters

### -param pulButtonsAvailable [out]

Receives the number of buttons available.

### -param pulCurrentButton [out]

Receives the number (from 1 through 36) of the currently selected button.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the pointer arguments is not valid.

</td>
</tr>
</table>

## -remarks

If buttons are not present, both <i>pulButtonsAvailable</i> and <i>pulCurrentButton</i> are set to zero.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-button-change">EC_DVD_BUTTON_CHANGE</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>