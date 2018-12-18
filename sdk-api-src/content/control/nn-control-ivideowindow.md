---
UID: NN:control.IVideoWindow
title: IVideoWindow
author: windows-sdk-content
description: The IVideoWindow interface sets properties on the video window.
old-location: dshow\ivideowindow.htm
tech.root: DirectShow
ms.assetid: 8e931c15-bd1d-409e-ada1-97fe49125fe7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], IVideoWindow interface [DirectShow],described, IVideoWindowInterface, control/IVideoWindow, dshow.ivideowindow
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow interface


## -description



The <code>IVideoWindow</code> interface sets properties on the video window. Applications can use it to set the window owner, the position and dimensions of the window, and other properties.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Dd390536(v=VS.85).aspx">IVMRWindowlessControl</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd390537(v=VS.85).aspx">IVMRWindowlessControl9</a> interface is now preferred over <code>IVideoWindow</code>. For more information, see <a href="https://msdn.microsoft.com/f53cecaa-dee7-4b02-a4ac-ffbd917f73aa">Using Windowless Mode</a>.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter and the Filter Graph Manager both expose this interface. The Filter Graph Manager forwards all method calls to the Video Renderer. It also forwards certain window messages that the Video Renderer needs to receive, such as <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a>. Because the video window is usually a child of an application window, the filter would not otherwise receive these messages. Therefore it relies on the Filter Graph Manager to forward them.

In most cases, an application should query the Filter Graph Manager for this interface, and not call the filter directly, because of the messaging issue just described. However, if the filter graph has more than one Video Renderer, the Filter Graph Manager only communicates with one of them, selected arbitrarily. Therefore, if your application uses multiple video windows, use the <code>IVideoWindow</code> interface directly on the filters. In that case, you must forward window messages to each Video Renderer instance, using the <a href="https://msdn.microsoft.com/en-us/library/Dd377312(v=VS.85).aspx">IVideoWindow::NotifyOwnerMessage</a> method.

To prevent the video window from flickering during repaints, override the default handling for the <a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a> message and do not erase the window. (For MFC applications, override <b>CWnd::OnEraseBkgnd</b> with an empty handler.)

Properties set on a video renderer persist between successive connections and disconnections.

Because this interface is Automation-compatible, all Boolean values are defined as OAFALSE (0) and OATRUE (–1).

<b>Error codes: </b>If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.

<b>Filter Developers: </b>You can use the <a href="https://msdn.microsoft.com/b6acec98-cff7-46ee-abd7-77f0b7ac3b9d">CBaseVideoWindow</a> class to help implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoWindow</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IVideoWindow</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd377290(v=VS.85).aspx">get_AutoShow</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377291(v=VS.85).aspx">get_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Queries whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377292(v=VS.85).aspx">get_BorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377293(v=VS.85).aspx">get_Caption</a>
</td>
<td align="left" width="63%">
Retrieves the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377294(v=VS.85).aspx">get_FullScreenMode</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer is in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377295(v=VS.85).aspx">get_Height</a>
</td>
<td align="left" width="63%">
Retrieves the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377296(v=VS.85).aspx">get_Left</a>
</td>
<td align="left" width="63%">
Retrieves the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377297(v=VS.85).aspx">get_MessageDrain</a>
</td>
<td align="left" width="63%">
Retrieves the window that receives mouse and keyboard messages from the video window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377298(v=VS.85).aspx">get_Owner</a>
</td>
<td align="left" width="63%">
Retrieves the video window's parent window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377299(v=VS.85).aspx">get_Top</a>
</td>
<td align="left" width="63%">
Retrieves the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377300(v=VS.85).aspx">get_Visible</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377301(v=VS.85).aspx">get_Width</a>
</td>
<td align="left" width="63%">
Retrieves the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377302(v=VS.85).aspx">get_WindowState</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible, hidden, minimized, or maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377303(v=VS.85).aspx">get_WindowStyle</a>
</td>
<td align="left" width="63%">
Retrieves the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377304(v=VS.85).aspx">get_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Retrieves the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377282(v=VS.85).aspx">GetMaxIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377284(v=VS.85).aspx">GetMinIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377286(v=VS.85).aspx">GetRestorePosition</a>
</td>
<td align="left" width="63%">
Retrieves the restored window position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377288(v=VS.85).aspx">GetWindowPosition</a>
</td>
<td align="left" width="63%">
Retrieves the position of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377306(v=VS.85).aspx">HideCursor</a>
</td>
<td align="left" width="63%">
Hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377308(v=VS.85).aspx">IsCursorHidden</a>
</td>
<td align="left" width="63%">
Queries whether the cursor is hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377312(v=VS.85).aspx">NotifyOwnerMessage</a>
</td>
<td align="left" width="63%">
Forwards a message to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377316(v=VS.85).aspx">put_AutoShow</a>
</td>
<td align="left" width="63%">
Specifies whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377317(v=VS.85).aspx">put_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Specifies whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377318(v=VS.85).aspx">put_BorderColor</a>
</td>
<td align="left" width="63%">
Sets the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377319(v=VS.85).aspx">put_Caption</a>
</td>
<td align="left" width="63%">
Sets the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377320(v=VS.85).aspx">put_FullScreenMode</a>
</td>
<td align="left" width="63%">
Enables or disables full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377321(v=VS.85).aspx">put_Height</a>
</td>
<td align="left" width="63%">
Sets the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377322(v=VS.85).aspx">put_Left</a>
</td>
<td align="left" width="63%">
Sets the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377323(v=VS.85).aspx">put_MessageDrain</a>
</td>
<td align="left" width="63%">
Specifies a window to receive mouse and keyboard messages from the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377324(v=VS.85).aspx">put_Owner</a>
</td>
<td align="left" width="63%">
Specifies a parent window for the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377325(v=VS.85).aspx">put_Top</a>
</td>
<td align="left" width="63%">
Sets the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377326(v=VS.85).aspx">put_Visible</a>
</td>
<td align="left" width="63%">
Shows or hides the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377327(v=VS.85).aspx">put_Width</a>
</td>
<td align="left" width="63%">
Sets the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377328(v=VS.85).aspx">put_WindowState</a>
</td>
<td align="left" width="63%">
Shows, hides, minimizes, or maximizes the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377329(v=VS.85).aspx">put_WindowStyle</a>
</td>
<td align="left" width="63%">
Sets the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377330(v=VS.85).aspx">put_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Sets the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377331(v=VS.85).aspx">SetWindowForeground</a>
</td>
<td align="left" width="63%">
Places the video window at the top of the Z order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377334(v=VS.85).aspx">SetWindowPosition</a>
</td>
<td align="left" width="63%">
Sets the position of the video window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

