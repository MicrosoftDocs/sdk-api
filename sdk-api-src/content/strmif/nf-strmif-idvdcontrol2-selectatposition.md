---
UID: NF:strmif.IDvdControl2.SelectAtPosition
title: IDvdControl2::SelectAtPosition (strmif.h)
description: The SelectAtPosition method highlights the menu button under the mouse pointer position.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectAtPosition method","IDvdControl2.SelectAtPosition","IDvdControl2::SelectAtPosition","IDvdControl2SelectAtPosition","SelectAtPosition","SelectAtPosition method [DirectShow]","SelectAtPosition method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectatposition","strmif/IDvdControl2::SelectAtPosition"]
old-location: dshow\idvdcontrol2_selectatposition.htm
tech.root: dshow
ms.assetid: f6cb9cb4-0792-43f5-b53b-02a38ccf0398
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectAtPosition method, IDvdControl2.SelectAtPosition, IDvdControl2::SelectAtPosition, IDvdControl2SelectAtPosition, SelectAtPosition, SelectAtPosition method [DirectShow], SelectAtPosition method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectatposition, strmif/IDvdControl2::SelectAtPosition
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
 - IDvdControl2::SelectAtPosition
 - strmif/IDvdControl2::SelectAtPosition
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
 - IDvdControl2.SelectAtPosition
---

# IDvdControl2::SelectAtPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectAtPosition</code> method highlights the menu button under the mouse pointer position.

## -parameters

### -param point [in]

Point on the screen, in screen pixel coordinates.

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
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button is present at the mouse pointer position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is in the Stop domain.

</td>
</tr>
</table>

## -remarks

Note that angle and menu button indexes are one-based while audio stream and subpicture stream indexes are zero-based.

Call <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-activatebutton">IDvdControl2::ActivateButton</a> in response to a mouse click when the pointer is over a menu button.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

This method is demonstrated in the DVDSample application in <b>CDvdCore::OnMouseEvent</b>.

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
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_FirstPlay</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>