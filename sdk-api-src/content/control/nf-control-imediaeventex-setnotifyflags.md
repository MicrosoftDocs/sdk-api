---
UID: NF:control.IMediaEventEx.SetNotifyFlags
title: IMediaEventEx::SetNotifyFlags (control.h)
description: The SetNotifyFlags method enables or disables event notifications.
helpviewer_keywords: ["IMediaEventEx interface [DirectShow]","SetNotifyFlags method","IMediaEventEx.SetNotifyFlags","IMediaEventEx::SetNotifyFlags","IMediaEventExSetNotifyFlags","SetNotifyFlags","SetNotifyFlags method [DirectShow]","SetNotifyFlags method [DirectShow]","IMediaEventEx interface","control/IMediaEventEx::SetNotifyFlags","dshow.imediaeventex_setnotifyflags"]
old-location: dshow\imediaeventex_setnotifyflags.htm
tech.root: dshow
ms.assetid: 6a41b6eb-3fe9-4b2e-bcbb-a407e0e6ab5e
ms.date: 4/26/2023
ms.keywords: IMediaEventEx interface [DirectShow],SetNotifyFlags method, IMediaEventEx.SetNotifyFlags, IMediaEventEx::SetNotifyFlags, IMediaEventExSetNotifyFlags, SetNotifyFlags, SetNotifyFlags method [DirectShow], SetNotifyFlags method [DirectShow],IMediaEventEx interface, control/IMediaEventEx::SetNotifyFlags, dshow.imediaeventex_setnotifyflags
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
 - IMediaEventEx::SetNotifyFlags
 - control/IMediaEventEx::SetNotifyFlags
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
 - IMediaEventEx.SetNotifyFlags
---

# IMediaEventEx::SetNotifyFlags


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetNotifyFlags</code> method enables or disables event notifications.

## -parameters

### -param lNoNotifyFlags [in]

Value indicating whether to enable or disable event notifications. Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Enable event notifications.</td>
</tr>
<tr>
<td>AM_MEDIAEVENT_NONOTIFY</td>
<td>Disable event notifications.</td>
</tr>
</table>

## -returns

Returns S_OK if successful, or E_INVALIDARG if the <i>lNoNotifyFlags</i> parameter is invalid.

## -remarks

By default, the Filter Graph Manager posts event notifications for the application. If the <i>lNoNotifyFlags</i> parameter is AM_MEDIAEVENT_NONOTIFY, the Filter Graph Manager clears any pending event notifications from the queue, and does not post any new ones.

If event notifications are disabled, the handle returned by the <a href="/windows/desktop/api/control/nf-control-imediaevent-geteventhandle">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> event.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx Interface</a>