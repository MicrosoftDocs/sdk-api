---
UID: NF:strmif.IDvdControl2.Pause
title: IDvdControl2::Pause (strmif.h)
description: Note  This method is deprecated. Applications should call IMediaControl::Pause instead. For more information, see Data Flow in the DVD Navigator. The Pause method pauses or resumes playback at the current location.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","Pause method","IDvdControl2.Pause","IDvdControl2::Pause","IDvdControl2Pause","Pause","Pause method [DirectShow]","Pause method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_pause","strmif/IDvdControl2::Pause"]
old-location: dshow\idvdcontrol2_pause.htm
tech.root: dshow
ms.assetid: 32ef572a-56f5-4aa4-b994-08f86a1f17ec
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],Pause method, IDvdControl2.Pause, IDvdControl2::Pause, IDvdControl2Pause, Pause, Pause method [DirectShow], Pause method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_pause, strmif/IDvdControl2::Pause
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
 - IDvdControl2::Pause
 - strmif/IDvdControl2::Pause
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
 - IDvdControl2.Pause
---

# IDvdControl2::Pause


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This method is deprecated. Applications should call <a href="/windows/desktop/api/control/nf-control-imediacontrol-pause">IMediaControl::Pause</a> instead. For more information, see <a href="/windows/desktop/DirectShow/data-flow-in-the-dvd-navigator">Data Flow in the DVD Navigator</a>.</div>
<div> </div>
The <code>Pause</code> method pauses or resumes playback at the current location.

## -parameters

### -param bState [in]

Value of type Boolean that specifies whether to pause playback; <b>TRUE</b> means to pause.

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
</table>

## -remarks

Putting the DVD Navigator into a paused state freezes playback and any internal timers, similar to <a href="/windows/desktop/api/control/nf-control-imediacontrol-pause">IMediaControl::Pause</a>. If the filter graph is not running, this method does nothing.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Pause_On, Pause_Off</td>
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