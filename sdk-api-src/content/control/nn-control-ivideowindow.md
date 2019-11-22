---
UID: NN:control.IVideoWindow
title: IVideoWindow (control.h)

description: The IVideoWindow interface sets properties on the video window.
old-location: dshow\ivideowindow.htm
tech.root: DirectShow
ms.assetid: 8e931c15-bd1d-409e-ada1-97fe49125fe7

ms.date: 12/05/2018
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], IVideoWindow interface [DirectShow],described, IVideoWindowInterface, control/IVideoWindow, dshow.ivideowindow
ms.topic: interface
f1_keywords: 
 - "control/IVideoWindow"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow interface


## -description



The <code>IVideoWindow</code> interface sets properties on the video window. Applications can use it to set the window owner, the position and dimensions of the window, and other properties.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> or <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9</a> interface is now preferred over <code>IVideoWindow</code>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-windowless-mode">Using Windowless Mode</a>.</div>
<div> </div>
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and the Filter Graph Manager both expose this interface. The Filter Graph Manager forwards all method calls to the Video Renderer. It also forwards certain window messages that the Video Renderer needs to receive, such as <a href="https://docs.microsoft.com/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a>. Because the video window is usually a child of an application window, the filter would not otherwise receive these messages. Therefore it relies on the Filter Graph Manager to forward them.

In most cases, an application should query the Filter Graph Manager for this interface, and not call the filter directly, because of the messaging issue just described. However, if the filter graph has more than one Video Renderer, the Filter Graph Manager only communicates with one of them, selected arbitrarily. Therefore, if your application uses multiple video windows, use the <code>IVideoWindow</code> interface directly on the filters. In that case, you must forward window messages to each Video Renderer instance, using the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-notifyownermessage">IVideoWindow::NotifyOwnerMessage</a> method.

To prevent the video window from flickering during repaints, override the default handling for the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message and do not erase the window. (For MFC applications, override <b>CWnd::OnEraseBkgnd</b> with an empty handler.)

Properties set on a video renderer persist between successive connections and disconnections.

Because this interface is Automation-compatible, all Boolean values are defined as OAFALSE (0) and OATRUE (–1).

<b>Error codes: </b>If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.

<b>Filter Developers: </b>You can use the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasevideowindow">CBaseVideoWindow</a> class to help implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoWindow</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IVideoWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVideoWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_autoshow">get_AutoShow</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_backgroundpalette">get_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Queries whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_bordercolor">get_BorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_caption">get_Caption</a>
</td>
<td align="left" width="63%">
Retrieves the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_fullscreenmode">get_FullScreenMode</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer is in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_height">get_Height</a>
</td>
<td align="left" width="63%">
Retrieves the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_left">get_Left</a>
</td>
<td align="left" width="63%">
Retrieves the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_messagedrain">get_MessageDrain</a>
</td>
<td align="left" width="63%">
Retrieves the window that receives mouse and keyboard messages from the video window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_owner">get_Owner</a>
</td>
<td align="left" width="63%">
Retrieves the video window's parent window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_top">get_Top</a>
</td>
<td align="left" width="63%">
Retrieves the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_visible">get_Visible</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_width">get_Width</a>
</td>
<td align="left" width="63%">
Retrieves the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_windowstate">get_WindowState</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible, hidden, minimized, or maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_windowstyle">get_WindowStyle</a>
</td>
<td align="left" width="63%">
Retrieves the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_windowstyleex">get_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Retrieves the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-getmaxidealimagesize">GetMaxIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-getminidealimagesize">GetMinIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-getrestoreposition">GetRestorePosition</a>
</td>
<td align="left" width="63%">
Retrieves the restored window position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-getwindowposition">GetWindowPosition</a>
</td>
<td align="left" width="63%">
Retrieves the position of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-hidecursor">HideCursor</a>
</td>
<td align="left" width="63%">
Hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-iscursorhidden">IsCursorHidden</a>
</td>
<td align="left" width="63%">
Queries whether the cursor is hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-notifyownermessage">NotifyOwnerMessage</a>
</td>
<td align="left" width="63%">
Forwards a message to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_autoshow">put_AutoShow</a>
</td>
<td align="left" width="63%">
Specifies whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_backgroundpalette">put_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Specifies whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_bordercolor">put_BorderColor</a>
</td>
<td align="left" width="63%">
Sets the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_caption">put_Caption</a>
</td>
<td align="left" width="63%">
Sets the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_fullscreenmode">put_FullScreenMode</a>
</td>
<td align="left" width="63%">
Enables or disables full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_height">put_Height</a>
</td>
<td align="left" width="63%">
Sets the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_left">put_Left</a>
</td>
<td align="left" width="63%">
Sets the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_messagedrain">put_MessageDrain</a>
</td>
<td align="left" width="63%">
Specifies a window to receive mouse and keyboard messages from the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_owner">put_Owner</a>
</td>
<td align="left" width="63%">
Specifies a parent window for the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_top">put_Top</a>
</td>
<td align="left" width="63%">
Sets the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_visible">put_Visible</a>
</td>
<td align="left" width="63%">
Shows or hides the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_width">put_Width</a>
</td>
<td align="left" width="63%">
Sets the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_windowstate">put_WindowState</a>
</td>
<td align="left" width="63%">
Shows, hides, minimizes, or maximizes the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_windowstyle">put_WindowStyle</a>
</td>
<td align="left" width="63%">
Sets the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_windowstyleex">put_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Sets the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-setwindowforeground">SetWindowForeground</a>
</td>
<td align="left" width="63%">
Places the video window at the top of the Z order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-setwindowposition">SetWindowPosition</a>
</td>
<td align="left" width="63%">
Sets the position of the video window.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

