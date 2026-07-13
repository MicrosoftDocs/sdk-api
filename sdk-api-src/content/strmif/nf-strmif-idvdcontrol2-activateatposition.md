---
UID: NF:strmif.IDvdControl2.ActivateAtPosition
title: IDvdControl2::ActivateAtPosition (strmif.h)
description: The ActivateAtPosition method activates the menu button under the mouse pointer position.
helpviewer_keywords: ["ActivateAtPosition","ActivateAtPosition method [DirectShow]","ActivateAtPosition method [DirectShow]","IDvdControl2 interface","IDvdControl2 interface [DirectShow]","ActivateAtPosition method","IDvdControl2.ActivateAtPosition","IDvdControl2::ActivateAtPosition","IDvdControl2ActivateAtPosition","dshow.idvdcontrol2_activateatposition","strmif/IDvdControl2::ActivateAtPosition"]
old-location: dshow\idvdcontrol2_activateatposition.htm
tech.root: dshow
ms.assetid: ff9eb02c-09c0-4b58-8e38-ec84ab1f1c42
ms.date: 4/26/2023
ms.keywords: ActivateAtPosition, ActivateAtPosition method [DirectShow], ActivateAtPosition method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],ActivateAtPosition method, IDvdControl2.ActivateAtPosition, IDvdControl2::ActivateAtPosition, IDvdControl2ActivateAtPosition, dshow.idvdcontrol2_activateatposition, strmif/IDvdControl2::ActivateAtPosition
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
 - IDvdControl2::ActivateAtPosition
 - strmif/IDvdControl2::ActivateAtPosition
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
 - IDvdControl2.ActivateAtPosition
---

# IDvdControl2::ActivateAtPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ActivateAtPosition</code> method activates the menu button under the mouse pointer position.

## -parameters

### -param point [in]

Point on the client window area, in screen pixel coordinates.

## -returns

Returns one of the following values.

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
The click occurred in the highlighted button rectangle, and the button was successfully activated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The point lies outside the valid video region.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The button is present but is not working.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not in a menu domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
There is no menu button under the mouse pointer position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
The operation is inhibited by user operation (UOP) control.

</td>
</tr>
</table>

## -remarks

The mouse pointer coordinates are relative to the upper left of the client area, which isn't necessarily the video display area if the video is in letterbox format.

Use this method when the user is navigating through a menu by moving the mouse pointer directly over the menu buttons. If the user is using the relative buttons to navigate the menu, use <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-activatebutton">ActivateButton</a> rather than <code>ActivateAtPosition</code>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>