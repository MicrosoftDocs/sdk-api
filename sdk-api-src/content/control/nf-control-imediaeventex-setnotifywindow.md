---
UID: NF:control.IMediaEventEx.SetNotifyWindow
title: IMediaEventEx::SetNotifyWindow (control.h)
description: The SetNotifyWindow method registers a window to process event notifications.
helpviewer_keywords: ["IMediaEventEx interface [DirectShow]","SetNotifyWindow method","IMediaEventEx.SetNotifyWindow","IMediaEventEx::SetNotifyWindow","IMediaEventExSetNotifyWindow","SetNotifyWindow","SetNotifyWindow method [DirectShow]","SetNotifyWindow method [DirectShow]","IMediaEventEx interface","control/IMediaEventEx::SetNotifyWindow","dshow.imediaeventex_setnotifywindow"]
old-location: dshow\imediaeventex_setnotifywindow.htm
tech.root: dshow
ms.assetid: 3e582c79-b8c7-40be-97fd-75d5b7965570
ms.date: 4/26/2023
ms.keywords: IMediaEventEx interface [DirectShow],SetNotifyWindow method, IMediaEventEx.SetNotifyWindow, IMediaEventEx::SetNotifyWindow, IMediaEventExSetNotifyWindow, SetNotifyWindow, SetNotifyWindow method [DirectShow], SetNotifyWindow method [DirectShow],IMediaEventEx interface, control/IMediaEventEx::SetNotifyWindow, dshow.imediaeventex_setnotifywindow
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
 - IMediaEventEx::SetNotifyWindow
 - control/IMediaEventEx::SetNotifyWindow
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
 - IMediaEventEx.SetNotifyWindow
---

# IMediaEventEx::SetNotifyWindow


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetNotifyWindow</code> method registers a window to process event notifications.

## -parameters

### -param hwnd [in]

Handle to the window, or <b>NULL</b> to stop receiving event messages.

### -param lMsg [in]

Window message to be passed as the notification.

### -param lInstanceData [in]

Value to be passed as the <i>lParam</i> parameter for the <i>lMsg</i> message.

## -returns

Returns S_OK if successful or E_INVALIDARG if the <i>hwnd</i> parameter is not a valid handle to a window.

## -remarks

This method designates a window that will process event notifications. Whenever the Filter Graph Manager puts an event in the event queue, it will also post a message to the designated window. The <i>hwnd</i> parameter specifies the window, and the <i>lMsg</i> parameter specifies the message. The application should define a private window message for this purpose. The message's <i>lParam</i> parameter is set to the value of <b>lInstanceData</b>, and the <i>wParam</i> parameter is set to zero.

When the window receives the message, it should call the <a href="/windows/desktop/api/control/nf-control-imediaevent-getevent">IMediaEvent::GetEvent</a> method to retrieve the event. Events are asynchronous, so the queue might contain several events (or none). Call <b>GetEvent</b> repeatedly, until it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx Interface</a>