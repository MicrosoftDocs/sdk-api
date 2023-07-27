---
UID: NF:control.IMediaEventEx.GetNotifyFlags
title: IMediaEventEx::GetNotifyFlags (control.h)
description: The GetNotifyFlags method determines whether event notifications are enabled.
helpviewer_keywords: ["GetNotifyFlags","GetNotifyFlags method [DirectShow]","GetNotifyFlags method [DirectShow]","IMediaEventEx interface","IMediaEventEx interface [DirectShow]","GetNotifyFlags method","IMediaEventEx.GetNotifyFlags","IMediaEventEx::GetNotifyFlags","IMediaEventExGetNotifyFlags","control/IMediaEventEx::GetNotifyFlags","dshow.imediaeventex_getnotifyflags"]
old-location: dshow\imediaeventex_getnotifyflags.htm
tech.root: dshow
ms.assetid: 797c5ee2-5a3c-4e95-b4b8-e29b39460ee0
ms.date: 4/26/2023
ms.keywords: GetNotifyFlags, GetNotifyFlags method [DirectShow], GetNotifyFlags method [DirectShow],IMediaEventEx interface, IMediaEventEx interface [DirectShow],GetNotifyFlags method, IMediaEventEx.GetNotifyFlags, IMediaEventEx::GetNotifyFlags, IMediaEventExGetNotifyFlags, control/IMediaEventEx::GetNotifyFlags, dshow.imediaeventex_getnotifyflags
req.header: control.h
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
 - IMediaEventEx::GetNotifyFlags
 - control/IMediaEventEx::GetNotifyFlags
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
 - IMediaEventEx.GetNotifyFlags
---

# IMediaEventEx::GetNotifyFlags


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNotifyFlags</code> method determines whether event notifications are enabled.

## -parameters

### -param lplNoNotifyFlags [out]

Pointer to a variable that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Event notifications are enabled.</td>
</tr>
<tr>
<td>AM_MEDIAEVENT_NONOTIFY</td>
<td>Event notifications are disabled.</td>
</tr>
</table>

## -returns

Returns S_OK if successful, or E_POINTER if the <i>lplNoNotifyFlags</i> parameter is <b>NULL</b>.

## -remarks

By default, the Filter Graph Manager posts event notifications for the application. To disable event notification, call the <a href="/windows/desktop/api/control/nf-control-imediaeventex-setnotifyflags">IMediaEventEx::SetNotifyFlags</a> method with the value AM_MEDIAEVENT_NONOTIFY.

If event notifications are disabled, the handle returned by the <a href="/windows/desktop/api/control/nf-control-imediaevent-geteventhandle">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> event.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx Interface</a>