---
UID: NN:shobjidl_core.IShellBrowser
title: IShellBrowser (shobjidl_core.h)
description: Implemented by hosts of Shell views (objects that implement IShellView). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window.
old-location: shell\IShellBrowser.htm
tech.root: shell
ms.assetid: 138d90e3-a1f0-4faf-88ca-16c7a46df0ca
ms.date: 12/05/2018
ms.keywords: IShellBrowser, IShellBrowser interface [Windows Shell], IShellBrowser interface [Windows Shell],described, _win32_IShellBrowser, shell.IShellBrowser, shobjidl_core/IShellBrowser
f1_keywords:
- shobjidl_core/IShellBrowser
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellBrowser interface


## -description


Implemented by hosts of Shell views (objects that implement <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>). Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window. 
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellBrowser</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IShellBrowser</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-browseobject">BrowseObject</a>
</td>
<td align="left" width="63%">
Informs Windows Explorer to browse to another folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-enablemodelesssb">EnableModelessSB</a>
</td>
<td align="left" width="63%">
Tells Windows Explorer to enable or disable its modeless dialog boxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getcontrolwindow">GetControlWindow</a>
</td>
<td align="left" width="63%">
Gets the window handle to a browser control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream">GetViewStateStream</a>
</td>
<td align="left" width="63%">
Gets an 
			<b>IStream</b> interface that can be used for storage of view-specific state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb">InsertMenusSB</a>
</td>
<td align="left" width="63%">
Allows the container to insert its menu groups into the composite menu that is displayed when an extended namespace is being viewed or used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive">OnViewWindowActive</a>
</td>
<td align="left" width="63%">
Called by the Shell view when the view window or one of its child windows gets the focus or becomes active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-queryactiveshellview">QueryActiveShellView</a>
</td>
<td align="left" width="63%">
Retrieves the currently active (displayed) Shell view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb">RemoveMenusSB</a>
</td>
<td align="left" width="63%">
Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg">SendControlMsg</a>
</td>
<td align="left" width="63%">
Sends control messages to either the toolbar or the status bar in a Windows Explorer window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb">SetMenuSB</a>
</td>
<td align="left" width="63%">
Installs the composite menu in the view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb">SetStatusTextSB</a>
</td>
<td align="left" width="63%">
Sets and displays status text about the in-place object in the container's frame-window status bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems">SetToolbarItems</a>
</td>
<td align="left" width="63%">
Adds toolbar items to Windows Explorer's toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a>
</td>
<td align="left" width="63%">
Translates accelerator keystrokes intended for the browser's frame while the view is active.

</td>
</tr>
</table> 


## -remarks



Windows Explorer and the <b>Open File</b> common dialog box are examples of implementations of this interface. It is a companion to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface exposed by extensions.



Objects that have access to the site chain of the browser can get a reference to the browser on <b>IShellBrowser</b> using  <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a>, with Service IDs such as SID_STopLevelBrowser and SID_SCommDlgBrowser. See the Knowledge Base article <a href="https://support.microsoft.com/kb/257717">Retrieve the Top-Level IWebBrowser2 Interface from an ActiveX Control</a> for more information on using service IDs.

<b>Windows 7 and later</b>.  Windows Explorer context menus  can support in-place navigation by using  <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a> with the Service ID SID_SlnPlaceBrowser.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
 

 

