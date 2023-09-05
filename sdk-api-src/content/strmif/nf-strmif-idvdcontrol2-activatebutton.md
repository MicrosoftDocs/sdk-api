---
UID: NF:strmif.IDvdControl2.ActivateButton
title: IDvdControl2::ActivateButton (strmif.h)
description: The ActivateButton method activates the currently selected menu button.
helpviewer_keywords: ["ActivateButton","ActivateButton method [DirectShow]","ActivateButton method [DirectShow]","IDvdControl2 interface","IDvdControl2 interface [DirectShow]","ActivateButton method","IDvdControl2.ActivateButton","IDvdControl2::ActivateButton","IDvdControl2ActivateButton","dshow.idvdcontrol2_activatebutton","strmif/IDvdControl2::ActivateButton"]
old-location: dshow\idvdcontrol2_activatebutton.htm
tech.root: dshow
ms.assetid: 20213874-ed28-4e0a-83af-044570b2c7e3
ms.date: 4/26/2023
ms.keywords: ActivateButton, ActivateButton method [DirectShow], ActivateButton method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],ActivateButton method, IDvdControl2.ActivateButton, IDvdControl2::ActivateButton, IDvdControl2ActivateButton, dshow.idvdcontrol2_activatebutton, strmif/IDvdControl2::ActivateButton
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
 - IDvdControl2::ActivateButton
 - strmif/IDvdControl2::ActivateButton
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
 - IDvdControl2.ActivateButton
---

# IDvdControl2::ActivateButton


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ActivateButton</code> method activates the currently selected menu button.



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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is in an invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the DVD Navigator from entering a paused state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button is selected.

</td>
</tr>
</table>

## -remarks

An application might or might not have four relative buttons on the side of the video display to represent the buttons on a physical remote control. These enable a user to select menu buttons but not activate them. A fifth button is required to activate the selected button. Call <code>ActivateButton</code> in response to a mouse click on the fifth button.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Button_Activate</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>
