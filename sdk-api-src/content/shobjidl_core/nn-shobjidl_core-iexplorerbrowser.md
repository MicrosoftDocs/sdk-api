---
UID: NN:shobjidl_core.IExplorerBrowser
title: IExplorerBrowser (shobjidl_core.h)
description: IExplorerBrowser is a browser object that can be either navigated or that can host a view of a data object. As a full-featured browser object, it also supports an automatic travel log.helpviewer_keywords: ["IExplorerBrowser","IExplorerBrowser interface [Windows Shell]","IExplorerBrowser interface [Windows Shell]","described","_shell_IExplorerBrowser","shell.IExplorerBrowser","shobjidl_core/IExplorerBrowser"]
old-location: shell\IExplorerBrowser.htm
tech.root: shell
ms.assetid: da2cf5d4-5a68-4d18-807b-b9d4e2712c10
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser, IExplorerBrowser interface [Windows Shell], IExplorerBrowser interface [Windows Shell],described, _shell_IExplorerBrowser, shell.IExplorerBrowser, shobjidl_core/IExplorerBrowser
f1_keywords:
- shobjidl_core/IExplorerBrowser
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IExplorerBrowser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerBrowser interface


## -description


<b>IExplorerBrowser</b> is a browser object that can be either navigated or that can host a view of a data object. As a full-featured browser object, it also supports an automatic travel log.

The Shell provides a default implementation of <b>IExplorerBrowser</b> as CLSID_ExplorerBrowser. Typically, a developer does not need to provide a custom implemention of this interface.

The Windows Software Development Kit (SDK) provides full samples that demonstrate the use of and interaction with <b>IExplorerBrowser</b>. Download the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940358(v=vs.85)">Explorer Browser Search Sample</a> and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940357(v=vs.85)">Explorer Browser Custom Contents Sample</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerBrowser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerBrowser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerBrowser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-advise">Advise</a>
</td>
<td align="left" width="63%">
Initiates a connection with <b>IExplorerBrowser</b> for event callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoidlist">BrowseToIDList</a>
</td>
<td align="left" width="63%">
Browses to a PIDL

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoobject">BrowseToObject</a>
</td>
<td align="left" width="63%">
Browses to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Destroys the browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject">FillFromObject</a>
</td>
<td align="left" width="63%">
Creates a results folder and fills it with items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getcurrentview">GetCurrentView</a>
</td>
<td align="left" width="63%">
Gets an interface for the current view of the browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current browser options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Prepares the browser to be navigated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all items from the results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setemptytext">SetEmptyText</a>
</td>
<td align="left" width="63%">
Sets the default empty text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setfoldersettings">SetFolderSettings</a>
</td>
<td align="left" width="63%">
Sets the folder settings for the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the current browser options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setpropertybag">SetPropertyBag</a>
</td>
<td align="left" width="63%">
Sets the name of the property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setrect">SetRect</a>
</td>
<td align="left" width="63%">
Sets the size and position of the view windows created by the browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection.

</td>
</tr>
</table> 


## -remarks



For example code that shows typical use of <b>IExplorerBrowser</b> and its methods, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940357(v=vs.85)">Explorer Browser Custom Contents</a> and Explorer Browser Custom Contents samples.

After calling this object's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-initialize">Initialize</a> method, its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-destroy">Destroy</a> method must be called to free any windowed resources that were generated in the call to <b>Initialize</b>.

The object that hosts the ExplorerBrowser object should derive from <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a> and implement <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> to respond to any queries for service. For example, the number of panes shown by the browser can be controlled by implementing <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility">IExplorerPaneVisibility</a> and responding to any SID_ExplorerPaneVisibility service requests.

Frames are disabled by default. To enable frames and get the default set of panes, set the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EBO_SHOWFRAMES</a> flag using the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions">IExplorerBrowser::SetOptions</a> method. The default panes, listed as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility">IExplorerPaneVisibility</a> constants, are these: 

                

<ul>
<li>EP_NavPane</li>
<li>EP_Commands</li>
<li>EP_Commands_Organize</li>
<li>EP_Commands_View</li>
<li>EP_DetailsPane</li>
<li>EP_PreviewPane</li>
<li>EP_QueryPane</li>
<li>EP_AdvQueryPane</li>
<li>EP_StatusBar</li>
<li>EP_Ribbon</li>
</ul>
See <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate">IExplorerPaneVisibility::GetPaneState</a> for more information.

Clients of the ExplorerBrowser object can implement the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-icommdlgbrowser3">ICommDlgBrowser3</a> interfaces and respond to an SID_SExplorerBrowserFrame service request in their QueryService implementations that are called when any <b>ICommDlgBrowser</b> interfaces are called on the browser (usually called from the view as a result of user actions). Note that the client does not receive a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser-includeobject">ICommDlgBrowser::IncludeObject</a> if a folder filter has been set on the browser by a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfiltersite-setfilter">IFolderFilterSite::SetFilter</a>.

To remain compatible with some older applications, the default Shell view (DefView) performs filtering operations (for example, searching operations executed by a search folder) on the UI thread. For new applications, this is typically not desired; the search should execute on a background thread. To stop the UI thread from filtering and instead run filtering on a background thread, provide <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a> through the SID_SExplorerBrowserFrame service request. When <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser2-getviewflags">ICommDlgBrowser2::GetViewFlags</a> is called, it should return CDB2GVF_NOINCLUDEITEM. For example, if you navigate to a search folder in ExplorerBrowser and you do not return CDB2GVF_NOINCLUDEITEM, the view can stop responding until the entire search is complete.

The Shell architecture has three main components: the browser, the views, and the data sources (for example, IShellFolder). The ExplorerBrowser object maintains the current location and navigation to other locations throughout the Shell namespace. It also keeps a travel log (forward and back history). The browser is notified when things happen in the view; for example, when the user double-clicks a folder. In response, the browser navigates to that location. The data sources are the objects that supply the items and folders in the namespace. They also have information about the location, such as the properties of the items and what to add to the context menu when the view requests it. Additionally, the data sources know what view should be created to represent their items at a location. In almost all instances, the folders create the Shell's default view (DefView). Therefore, as the browser navigates, it receives an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object for the new location and asks it what view to create. The browser then creates that view and makes it visible, while hiding and then destroying the view that was showing the previous location. The view is responsible for communicating with <b>IShellFolder</b> for the current location and requesting it to enumerate the items, which allows the view to show these items to the user. As the user interacts with the items, the view communicates with the <b>IShellFolder</b> to get any additional information it needs, such as specific properties of the items or the context menu entries for the item.

If an application uses the default implementation provided by CLSID_ExplorerBrowser, inserting it into the window of an application and then browsing to a location, ExplorerBrowser creates the proper <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> as specified by the location that it is browsing to. The application can then ask ExplorerBrowser to give it an interface on the current view, allowing the application to manipulate the view directly if required. The default implementation of the Windows Explorer view object, created by <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>, supports the interface <b>IShellView</b>. You may verify that you have the default Shell folder view object by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getcurrentview">IExplorerBrowser::GetCurrentView</a> and then calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the object returned using the interface ID IID_CDefView.

<b>Windows 7 and later</b>. CExplorerBrowser can support in-place navigation by using <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a> with the Service ID SID_SlnPlaceBrowser. When using SID_SInPlaceBrowser, the CExplorerBrowser state cannot be set to EBO_NAVIGATEONCE.



