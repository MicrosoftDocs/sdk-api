---
UID: NN:control.IVideoWindow
title: IVideoWindow (control.h)
description: The IVideoWindow interface sets properties on the video window.
helpviewer_keywords: ["IVideoWindow","IVideoWindow interface [DirectShow]","IVideoWindow interface [DirectShow]","described","IVideoWindowInterface","control/IVideoWindow","dshow.ivideowindow"]
old-location: dshow\ivideowindow.htm
tech.root: dshow
ms.assetid: 8e931c15-bd1d-409e-ada1-97fe49125fe7
ms.date: 4/26/2023
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], IVideoWindow interface [DirectShow],described, IVideoWindowInterface, control/IVideoWindow, dshow.ivideowindow
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
 - IVideoWindow
 - control/IVideoWindow
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
 - IVideoWindow
---

# IVideoWindow interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVideoWindow</code> interface sets properties on the video window. Applications can use it to set the window owner, the position and dimensions of the window, and other properties.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> or <a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9</a> interface is now preferred over <code>IVideoWindow</code>. For more information, see <a href="/windows/desktop/DirectShow/using-windowless-mode">Using Windowless Mode</a>.</div>
<div> </div>
The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and the Filter Graph Manager both expose this interface. The Filter Graph Manager forwards all method calls to the Video Renderer. It also forwards certain window messages that the Video Renderer needs to receive, such as <a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a>. Because the video window is usually a child of an application window, the filter would not otherwise receive these messages. Therefore it relies on the Filter Graph Manager to forward them.

In most cases, an application should query the Filter Graph Manager for this interface, and not call the filter directly, because of the messaging issue just described. However, if the filter graph has more than one Video Renderer, the Filter Graph Manager only communicates with one of them, selected arbitrarily. Therefore, if your application uses multiple video windows, use the <code>IVideoWindow</code> interface directly on the filters. In that case, you must forward window messages to each Video Renderer instance, using the <a href="/windows/desktop/api/control/nf-control-ivideowindow-notifyownermessage">IVideoWindow::NotifyOwnerMessage</a> method.

To prevent the video window from flickering during repaints, override the default handling for the <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message and do not erase the window. (For MFC applications, override <b>CWnd::OnEraseBkgnd</b> with an empty handler.)

Properties set on a video renderer persist between successive connections and disconnections.

Because this interface is Automation-compatible, all Boolean values are defined as OAFALSE (0) and OATRUE (–1).

<b>Error codes: </b>If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.

<b>Filter Developers: </b>You can use the <a href="/windows/desktop/DirectShow/cbasevideowindow">CBaseVideoWindow</a> class to help implement this interface.

## -inheritance

The <b>IVideoWindow</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IVideoWindow</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
