---
UID: NF:shobjidl_core.IExplorerBrowser.FillFromObject
title: IExplorerBrowser::FillFromObject (shobjidl_core.h)
description: Creates a results folder and fills it with items.
helpviewer_keywords: ["FillFromObject","FillFromObject method [Windows Shell]","FillFromObject method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","FillFromObject method","IExplorerBrowser.FillFromObject","IExplorerBrowser::FillFromObject","_shell_IExplorerBrowser_FillFromObject","shell.IExplorerBrowser_FillFromObject","shobjidl_core/IExplorerBrowser::FillFromObject"]
old-location: shell\IExplorerBrowser_FillFromObject.htm
tech.root: shell
ms.assetid: f978d5d1-a597-4e49-9a2a-de23e99bf65e
ms.date: 12/05/2018
ms.keywords: FillFromObject, FillFromObject method [Windows Shell], FillFromObject method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],FillFromObject method, IExplorerBrowser.FillFromObject, IExplorerBrowser::FillFromObject, _shell_IExplorerBrowser_FillFromObject, shell.IExplorerBrowser_FillFromObject, shobjidl_core/IExplorerBrowser::FillFromObject
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
 - IExplorerBrowser::FillFromObject
 - shobjidl_core/IExplorerBrowser::FillFromObject
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
 - IExplorerBrowser.FillFromObject
---

# IExplorerBrowser::FillFromObject


## -description

Creates a results folder and fills it with items.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

An interface pointer on the source object that will fill the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iresultsfolder">IResultsFolder</a>. This can be an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> or any object that can be used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EXPLORER_BROWSER_FILL_FLAGS</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EXPLORER_BROWSER_FILL_FLAGS</a> values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The object passed via interface pointer <i>punk</i> fills <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iresultsfolder">IResultsFolder</a>.

The parameter <i>dwFlags</i> can be any of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EXPLORER_BROWSER_FILL_FLAGS</a> or any of the flags defined in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-browseobject">BrowseObject</a>'s <i>wFlags</i> parameter, except for flags that indicate navigation.

The parameter <i>punk</i> can be any object that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a> can consume.  If called with <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EBF_SELECTFROMDATAOBJECT</a>, <i>punk</i> must be an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> and the namespace will be walked at the parent level of the data object, including all peer items, but selecting only those contained in the data object. This flag is most commonly used when <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> have <i>FWF_CHECKSELECT</i> enabled, allowing check-selection of a set of items that have been compiled in the data object.

<div class="alert"><b>Note</b>  If a pointer to an item identifier list (PIDL) in the data object is fully qualified, the parent folder cannot be successfully walked, because desktop folder items would be added to the list.</div>
<div> </div>
This method may be called more than once, with each successive call adding additional items to the view. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-removeall">IExplorerBrowser::RemoveAll</a> may be called to clear the contents of the results folder. This function should be called with <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags">EBF_NODROPTARGET</a> to prevent users from drag dropping new items into the view, unless this is desired.  Setting <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EBO_NAVIGATEONCE</a> is also recommended so that the browser will stay in the ResultsFolder, preventing the user from navigating to a folder that may be represented in the data object.

To manipulate items in the results folder directly, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getcurrentview">IExplorerBrowser::GetCurrentView</a> to get the view from ExplorerBrowser and then ask the view for results folder using <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder">GetFolder</a>. Using the obtained results folder enables manipulation of the data in the folder with more flexibility than with the methods that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> provides.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>