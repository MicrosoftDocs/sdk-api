---
UID: NF:shobjidl_core.IExplorerBrowser.BrowseToObject
title: IExplorerBrowser::BrowseToObject (shobjidl_core.h)
description: Browses to an object.
helpviewer_keywords: ["BrowseToObject","BrowseToObject method [Windows Shell]","BrowseToObject method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","BrowseToObject method","IExplorerBrowser.BrowseToObject","IExplorerBrowser::BrowseToObject","SBSP_ABSOLUTE","SBSP_KEEPWORDWHEELTEXT","SBSP_NAVIGATEBACK","SBSP_NAVIGATEFORWARD","SBSP_PARENT","SBSP_RELATIVE","_shell_IExplorerBrowser_BrowseToObject","shell.IExplorerBrowser_BrowseToObject","shobjidl_core/IExplorerBrowser::BrowseToObject"]
old-location: shell\IExplorerBrowser_BrowseToObject.htm
tech.root: shell
ms.assetid: cbfe2348-9fdc-4839-bf8b-b2a65caefa4c
ms.date: 12/05/2018
ms.keywords: BrowseToObject, BrowseToObject method [Windows Shell], BrowseToObject method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],BrowseToObject method, IExplorerBrowser.BrowseToObject, IExplorerBrowser::BrowseToObject, SBSP_ABSOLUTE, SBSP_KEEPWORDWHEELTEXT, SBSP_NAVIGATEBACK, SBSP_NAVIGATEFORWARD, SBSP_PARENT, SBSP_RELATIVE, _shell_IExplorerBrowser_BrowseToObject, shell.IExplorerBrowser_BrowseToObject, shobjidl_core/IExplorerBrowser::BrowseToObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExplorerBrowser::BrowseToObject
 - shobjidl_core/IExplorerBrowser::BrowseToObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.BrowseToObject
---

# IExplorerBrowser::BrowseToObject


## -description

Browses to an object.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an object to browse to. If the object cannot be browsed, an error value is returned.

### -param uFlags [in]

Type: <b>UINT</b>

A flag that specifies the category of the <i>pidl</i>. This affects how navigation is accomplished. Must be the value zero, or a bitwise combination of the following values.



#### SBSP_ABSOLUTE

An absolute PIDL, relative to the desktop.



#### SBSP_RELATIVE

A relative PIDL, relative to the current folder.



#### SBSP_PARENT

Browse the parent folder, ignore the PIDL.



#### SBSP_NAVIGATEBACK

Navigate back, ignore the PIDL.



#### SBSP_NAVIGATEFORWARD

Navigate forward, ignore the PIDL.





#### SBSP_KEEPWORDWHEELTEXT

<b>Windows Vista and later</b>. This flag indicates that any search text entered by a WordWheel (the Search box in Windows Explorer) should be preserved during this navigation, so that items at the new location are filtered in the same way they were filtered at the previous location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<i>uFlags</i> may be any of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EXPLORER_BROWSER_FILL_FLAGS</a> or any of the flags defined in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-browseobject">BrowseObject</a>'s <i>wFlags</i> parameter, except for flags that indicate navigation.

This method calls <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-getidlist">GetIDList</a> and browses to the pidl returned.  It operates in the same way as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoidlist">IExplorerBrowser::BrowseToIDList</a>, except that <i>punk</i> cannot be <b>NULL</b>. Standard usage is to browse to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>. An error will be returned if the object passed in cannot be browsed through. An object that can be browsed through implements either <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a>.

The first navigation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> is synchronous. After that, all navigations are asynchronous. As a result, calls to <b>IExplorerBrowser::BrowseToObject</b> will succeed if you properly set up the pending   navigation, but that does not guarantee the navigation will succeed.  To be informed of success and failure, clients should implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents">IExplorerBrowserEvents</a> and respond appropriately in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">OnNavigationComplete</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">OnNavigationFailed</a>.