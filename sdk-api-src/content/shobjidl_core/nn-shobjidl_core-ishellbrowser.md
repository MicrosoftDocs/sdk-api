---
UID: NN:shobjidl_core.IShellBrowser
title: IShellBrowser
author: windows-sdk-content
description: Implemented by hosts of Shell views (objects that implement IShellView). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window.
old-location: shell\IShellBrowser.htm
tech.root: shell
ms.assetid: 138d90e3-a1f0-4faf-88ca-16c7a46df0ca
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IShellBrowser, IShellBrowser interface [Windows Shell], IShellBrowser interface [Windows Shell],described, _win32_IShellBrowser, shell.IShellBrowser, shobjidl_core/IShellBrowser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellBrowser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellBrowser interface


## -description


Implemented by hosts of Shell views (objects that implement <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window. 
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellBrowser</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IShellBrowser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellBrowser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e391ca11-25e3-4d97-8efd-0afd74a3e5c2">BrowseObject</a>
</td>
<td align="left" width="63%">
Informs Windows Explorer to browse to another folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bf39e3f-8b17-4307-ba57-7363c006c34b">EnableModelessSB</a>
</td>
<td align="left" width="63%">
Tells Windows Explorer to enable or disable its modeless dialog boxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ddcdafd-01f6-441c-9cc8-1ca9f1209e25">GetControlWindow</a>
</td>
<td align="left" width="63%">
Gets the window handle to a browser control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/887ebe9f-8bde-46dd-a7a2-7b2ca66bf905">GetViewStateStream</a>
</td>
<td align="left" width="63%">
Gets an 
			<b>IStream</b> interface that can be used for storage of view-specific state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62cbb593-7459-4a4f-96a2-3ec2287e6a26">InsertMenusSB</a>
</td>
<td align="left" width="63%">
Allows the container to insert its menu groups into the composite menu that is displayed when an extended namespace is being viewed or used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd320262-f383-453b-9028-4e93f0b3761a">OnViewWindowActive</a>
</td>
<td align="left" width="63%">
Called by the Shell view when the view window or one of its child windows gets the focus or becomes active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d03e41dc-72dc-4f34-ae5b-b5ef8b2f146d">QueryActiveShellView</a>
</td>
<td align="left" width="63%">
Retrieves the currently active (displayed) Shell view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa96ac59-62cd-4010-8a0f-b743527f61da">RemoveMenusSB</a>
</td>
<td align="left" width="63%">
Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4494870b-45a8-478a-807a-7ed3674f69f3">SendControlMsg</a>
</td>
<td align="left" width="63%">
Sends control messages to either the toolbar or the status bar in a Windows Explorer window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae6fe864-7fa1-4c74-a27f-d428bdeccc3d">SetMenuSB</a>
</td>
<td align="left" width="63%">
Installs the composite menu in the view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7dd9f17-41e4-4c04-981e-a0bfe7c53fcf">SetStatusTextSB</a>
</td>
<td align="left" width="63%">
Sets and displays status text about the in-place object in the container's frame-window status bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff141d3-e175-464a-9869-317d547e7489">SetToolbarItems</a>
</td>
<td align="left" width="63%">
Adds toolbar items to Windows Explorer's toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a>
</td>
<td align="left" width="63%">
Translates accelerator keystrokes intended for the browser's frame while the view is active.

</td>
</tr>
</table> 


## -remarks



Windows Explorer and the <b>Open File</b> common dialog box are examples of implementations of this interface. It is a companion to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface exposed by extensions.



Objects that have access to the site chain of the browser can get a reference to the browser on <b>IShellBrowser</b> using  <a href="_inet_IServiceProvider_QueryService_Method">IServiceProvider::QueryService</a>, with Service IDs such as SID_STopLevelBrowser and SID_SCommDlgBrowser. See the Knowledge Base article <a href="http://go.microsoft.com/fwlink/p/?linkid=200322">Retrieve the Top-Level IWebBrowser2 Interface from an ActiveX Control</a> for more information on using service IDs.

<b>Windows 7 and later</b>.  Windows Explorer context menus  can support in-place navigation by using  <a href="_inet_IServiceProvider_QueryService_Method">IServiceProvider::QueryService</a> with the Service ID SID_SlnPlaceBrowser.




## -see-also




<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>



<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

