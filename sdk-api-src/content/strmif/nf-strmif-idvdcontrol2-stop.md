---
UID: NF:strmif.IDvdControl2.Stop
title: IDvdControl2::Stop (strmif.h)
description: The Stop method stops playback of a title or menu by moving the DVD Navigator into the DVD Stop domain.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","Stop method","IDvdControl2.Stop","IDvdControl2::Stop","IDvdControl2Stop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_stop","strmif/IDvdControl2::Stop"]
old-location: dshow\idvdcontrol2_stop.htm
tech.root: dshow
ms.assetid: 9c1ebe2b-c40a-410f-a4a5-ad79350a27dd
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],Stop method, IDvdControl2.Stop, IDvdControl2::Stop, IDvdControl2Stop, Stop, Stop method [DirectShow], Stop method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_stop, strmif/IDvdControl2::Stop
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
 - IDvdControl2::Stop
 - strmif/IDvdControl2::Stop
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
 - IDvdControl2.Stop
---

# IDvdControl2::Stop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Stop</code> method stops playback of a title or menu by moving the DVD Navigator into the DVD Stop domain.



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
Invalid domain.

</td>
</tr>
</table>

## -remarks

Calling this method puts the DVD Navigator into the Stop domain, but the DVD filter graph as a whole remains in a running state, ready to play at any time. From the Stop, domain the user can display a menu or initiate playback directly through any "Play" method.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Stop</td>
<td>
<ul>
<li>DVD_DOMAIN_FirstPlay</li>
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
