---
UID: NN:control.IVideoWindow
title: IVideoWindow
author: windows-sdk-content
description: The IVideoWindow interface sets properties on the video window.
old-location: dshow\ivideowindow.htm
old-project: DirectShow
ms.assetid: 8e931c15-bd1d-409e-ada1-97fe49125fe7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], IVideoWindow interface [DirectShow],described, IVideoWindowInterface, control/IVideoWindow, dshow.ivideowindow
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVideoWindow
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow interface


## -description



The <code>IVideoWindow</code> interface sets properties on the video window. Applications can use it to set the window owner, the position and dimensions of the window, and other properties.

<div class="alert"><b>Note</b>  
           The <a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl</a> or <a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9</a> interface is now preferred over <code>IVideoWindow</code>. For more information, see <a href="https://msdn.microsoft.com/f53cecaa-dee7-4b02-a4ac-ffbd917f73aa">Using Windowless Mode</a>.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter and the Filter Graph Manager both expose this interface. The Filter Graph Manager forwards all method calls to the Video Renderer. It also forwards certain window messages that the Video Renderer needs to receive, such as <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a>. Because the video window is usually a child of an application window, the filter would not otherwise receive these messages. Therefore it relies on the Filter Graph Manager to forward them.

In most cases, an application should query the Filter Graph Manager for this interface, and not call the filter directly, because of the messaging issue just described. However, if the filter graph has more than one Video Renderer, the Filter Graph Manager only communicates with one of them, selected arbitrarily. Therefore, if your application uses multiple video windows, use the <code>IVideoWindow</code> interface directly on the filters. In that case, you must forward window messages to each Video Renderer instance, using the <a href="https://msdn.microsoft.com/37d28f32-5da5-4082-ac57-5b274e95ca68">IVideoWindow::NotifyOwnerMessage</a> method.

To prevent the video window from flickering during repaints, override the default handling for the <a href="winui._win32_WM_ERASEBKGND">WM_ERASEBKGND</a> message and do not erase the window. (For MFC applications, override <b>CWnd::OnEraseBkgnd</b> with an empty handler.)

Properties set on a video renderer persist between successive connections and disconnections.

Because this interface is Automation-compatible, all Boolean values are defined as OAFALSE (0) and OATRUE (–1).

<b>Error codes: </b>If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.

<b>Filter Developers: </b>You can use the <a href="https://msdn.microsoft.com/b6acec98-cff7-46ee-abd7-77f0b7ac3b9d">CBaseVideoWindow</a> class to help implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVideoWindow</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IVideoWindow</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6f42e37d-af67-4f9e-8a02-d1f4154df391">get_AutoShow</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdd11f60-e042-4aad-a867-d1e12a88ebfe">get_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Queries whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f2df219-6b82-41fa-b0a9-251cc54fe019">get_BorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbb42e55-1be1-4931-869b-9e8d4af5e6df">get_Caption</a>
</td>
<td align="left" width="63%">
Retrieves the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/742587c7-545a-4c5f-bff1-511ed6d0b1d5">get_FullScreenMode</a>
</td>
<td align="left" width="63%">
Queries whether the video renderer is in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1d29cd5-1e82-4406-b007-aa7b581d158e">get_Height</a>
</td>
<td align="left" width="63%">
Retrieves the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d75c926-588c-4fb2-b537-f27602799b2e">get_Left</a>
</td>
<td align="left" width="63%">
Retrieves the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a1a3070-5b68-4dd2-bc10-97a8331cc262">get_MessageDrain</a>
</td>
<td align="left" width="63%">
Retrieves the window that receives mouse and keyboard messages from the video window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bb21c2a-25c6-43fa-a1b0-9f09944f1326">get_Owner</a>
</td>
<td align="left" width="63%">
Retrieves the video window's parent window, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00baab45-d740-4f74-bd53-eb2ff21c5dcc">get_Top</a>
</td>
<td align="left" width="63%">
Retrieves the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b533398e-80f6-4f33-982b-93b8e0d705e9">get_Visible</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/179b065a-7269-40fa-8772-b336f27d69de">get_Width</a>
</td>
<td align="left" width="63%">
Retrieves the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecda497c-634b-4a7e-9f21-85bde307c796">get_WindowState</a>
</td>
<td align="left" width="63%">
Queries whether the video window is visible, hidden, minimized, or maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae4ae516-743f-4a27-90d5-108ca26aadd4">get_WindowStyle</a>
</td>
<td align="left" width="63%">
Retrieves the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdffe918-5802-406e-86b1-d1e9ebb6dbf7">get_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Retrieves the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee9f6803-c8b8-48e0-9be0-3d61a453014e">GetMaxIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2d1d267-008d-402a-864a-e801e7581fbd">GetMinIdealImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum ideal size for the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2c8880a-e140-4bb1-8f0d-2d665c98728c">GetRestorePosition</a>
</td>
<td align="left" width="63%">
Retrieves the restored window position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df55c10d-aec1-42f3-8bfb-207ae8804e72">GetWindowPosition</a>
</td>
<td align="left" width="63%">
Retrieves the position of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c45da114-6711-427b-8533-4ed339a42ff4">HideCursor</a>
</td>
<td align="left" width="63%">
Hides the cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/240040d8-433e-4398-a20a-66cc5a27bdae">IsCursorHidden</a>
</td>
<td align="left" width="63%">
Queries whether the cursor is hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37d28f32-5da5-4082-ac57-5b274e95ca68">NotifyOwnerMessage</a>
</td>
<td align="left" width="63%">
Forwards a message to the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7481a7e8-4b57-43cc-8304-b70616bbd532">put_AutoShow</a>
</td>
<td align="left" width="63%">
Specifies whether the video renderer automatically shows the video window when it receives video data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b1d34b6-0043-4929-a496-cf84b5d47b55">put_BackgroundPalette</a>
</td>
<td align="left" width="63%">
Specifies whether the video window realizes its palette in the background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0e249f4-4a17-4c5d-8f16-bb1aceef2064">put_BorderColor</a>
</td>
<td align="left" width="63%">
Sets the color that appears around the edges of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d16dca01-95ba-4573-b9c4-ab996dcf21e4">put_Caption</a>
</td>
<td align="left" width="63%">
Sets the video window caption.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efa1c6ed-bea5-4c25-89c2-1b6fcdad3834">put_FullScreenMode</a>
</td>
<td align="left" width="63%">
Enables or disables full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ba411f-675f-4dad-be4f-6beffbd3b53c">put_Height</a>
</td>
<td align="left" width="63%">
Sets the height of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a614ee46-49cf-40e4-a1f7-b3b3b7065175">put_Left</a>
</td>
<td align="left" width="63%">
Sets the video window's x-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaf8624c-b3ea-4034-845a-6cd74c725c44">put_MessageDrain</a>
</td>
<td align="left" width="63%">
Specifies a window to receive mouse and keyboard messages from the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/658ad234-cb5a-428b-ae19-0cd52db6718b">put_Owner</a>
</td>
<td align="left" width="63%">
Specifies a parent window for the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a5df1f1-3867-4956-8e1b-090aa8d8ff3a">put_Top</a>
</td>
<td align="left" width="63%">
Sets the video window's y-coordinate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae789f07-4d50-488c-b57e-2b003a8cde3e">put_Visible</a>
</td>
<td align="left" width="63%">
Shows or hides the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cb02033-0405-4b8b-91fc-2f33097f2c88">put_Width</a>
</td>
<td align="left" width="63%">
Sets the width of the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75189754-61c4-4196-9cfb-3f8c8e33efbc">put_WindowState</a>
</td>
<td align="left" width="63%">
Shows, hides, minimizes, or maximizes the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd1422d1-16a3-4aae-aadb-772a06173ba3">put_WindowStyle</a>
</td>
<td align="left" width="63%">
Sets the window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19d56e9d-6f6d-46aa-b46f-a62302b41d2f">put_WindowStyleEx</a>
</td>
<td align="left" width="63%">
Sets the extended window style on the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff4f3707-1f2e-499b-8108-81616fe4ae9b">SetWindowForeground</a>
</td>
<td align="left" width="63%">
Places the video window at the top of the Z order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e667044-1781-4380-b855-d15cf8cd2349">SetWindowPosition</a>
</td>
<td align="left" width="63%">
Sets the position of the video window.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

