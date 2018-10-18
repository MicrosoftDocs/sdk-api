---
UID: NF:shobjidl_core.IExplorerBrowser.FillFromObject
title: IExplorerBrowser::FillFromObject
author: windows-sdk-content
description: Creates a results folder and fills it with items.
old-location: shell\IExplorerBrowser_FillFromObject.htm
tech.root: shell
ms.assetid: f978d5d1-a597-4e49-9a2a-de23e99bf65e
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: FillFromObject, FillFromObject method [Windows Shell], FillFromObject method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],FillFromObject method, IExplorerBrowser.FillFromObject, IExplorerBrowser::FillFromObject, _shell_IExplorerBrowser_FillFromObject, shell.IExplorerBrowser_FillFromObject, shobjidl_core/IExplorerBrowser::FillFromObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IExplorerBrowser.FillFromObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerBrowser::FillFromObject


## -description


Creates a results folder and fills it with items.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

An interface pointer on the source object that will fill the <a href="https://msdn.microsoft.com/db44052b-bd26-412f-9f2a-66a0c53b65ac">IResultsFolder</a>. This can be an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> or any object that can be used with <a href="https://msdn.microsoft.com/164732ae-1c72-465c-a16b-a8eeaa9cc185">INamespaceWalk</a>.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/5be62600-147d-4625-8e6c-aa6687da2168">EXPLORER_BROWSER_FILL_FLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/5be62600-147d-4625-8e6c-aa6687da2168">EXPLORER_BROWSER_FILL_FLAGS</a> values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The object passed via interface pointer <i>punk</i> fills <a href="https://msdn.microsoft.com/db44052b-bd26-412f-9f2a-66a0c53b65ac">IResultsFolder</a>.

The parameter <i>dwFlags</i> can be any of the <a href="https://msdn.microsoft.com/5be62600-147d-4625-8e6c-aa6687da2168">EXPLORER_BROWSER_FILL_FLAGS</a> or any of the flags defined in <a href="https://msdn.microsoft.com/e391ca11-25e3-4d97-8efd-0afd74a3e5c2">BrowseObject</a>'s <i>wFlags</i> parameter, except for flags that indicate navigation.

The parameter <i>punk</i> can be any object that <a href="https://msdn.microsoft.com/164732ae-1c72-465c-a16b-a8eeaa9cc185">INamespaceWalk</a> can consume.  If called with <a href="https://msdn.microsoft.com/5be62600-147d-4625-8e6c-aa6687da2168">EBF_SELECTFROMDATAOBJECT</a>, <i>punk</i> must be an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> and the namespace will be walked at the parent level of the data object, including all peer items, but selecting only those contained in the data object. This flag is most commonly used when <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> have <i>FWF_CHECKSELECT</i> enabled, allowing check-selection of a set of items that have been compiled in the data object.

<div class="alert"><b>Note</b>  If a pointer to an item identifier list (PIDL) in the data object is fully qualified, the parent folder cannot be successfully walked, because desktop folder items would be added to the list.</div>
<div> </div>
This method may be called more than once, with each successive call adding additional items to the view. <a href="https://msdn.microsoft.com/4447d3f4-659f-4ec1-8a6f-91031c85b704">IExplorerBrowser::RemoveAll</a> may be called to clear the contents of the results folder. This function should be called with <a href="https://msdn.microsoft.com/5be62600-147d-4625-8e6c-aa6687da2168">EBF_NODROPTARGET</a> to prevent users from drag dropping new items into the view, unless this is desired.  Setting <a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EBO_NAVIGATEONCE</a> is also recommended so that the browser will stay in the ResultsFolder, preventing the user from navigating to a folder that may be represented in the data object.

To manipulate items in the results folder directly, call <a href="https://msdn.microsoft.com/e7c05a67-f739-487d-872a-3598b790d5c9">IExplorerBrowser::GetCurrentView</a> to get the view from ExplorerBrowser and then ask the view for results folder using <a href="https://msdn.microsoft.com/4fdeb995-2220-4461-a4d6-80bce08153b1">GetFolder</a>. Using the obtained results folder enables manipulation of the data in the folder with more flexibility than with the methods that <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> provides.




## -see-also




<a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>



<a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a>
 

 

