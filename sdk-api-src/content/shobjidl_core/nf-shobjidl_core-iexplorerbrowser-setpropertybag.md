---
UID: NF:shobjidl_core.IExplorerBrowser.SetPropertyBag
title: IExplorerBrowser::SetPropertyBag (shobjidl_core.h)
description: Sets the name of the property bag.
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","SetPropertyBag method","IExplorerBrowser.SetPropertyBag","IExplorerBrowser::SetPropertyBag","SetPropertyBag","SetPropertyBag method [Windows Shell]","SetPropertyBag method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_SetPropertyBag","shell.IExplorerBrowser_SetPropertyBag","shobjidl_core/IExplorerBrowser::SetPropertyBag"]
old-location: shell\IExplorerBrowser_SetPropertyBag.htm
tech.root: shell
ms.assetid: e43cc4a0-2ff4-42a2-ac60-78a884c37d75
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetPropertyBag method, IExplorerBrowser.SetPropertyBag, IExplorerBrowser::SetPropertyBag, SetPropertyBag, SetPropertyBag method [Windows Shell], SetPropertyBag method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetPropertyBag, shell.IExplorerBrowser_SetPropertyBag, shobjidl_core/IExplorerBrowser::SetPropertyBag
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
 - IExplorerBrowser::SetPropertyBag
 - shobjidl_core/IExplorerBrowser::SetPropertyBag
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
 - IExplorerBrowser.SetPropertyBag
---

# IExplorerBrowser::SetPropertyBag


## -description

Sets the name of the property bag.

## -parameters

### -param pszPropertyBag [in]

Type: <b>LPCWSTR</b>

A pointer to a constant, null-terminated, Unicode string that contains the name of the property bag.
                   View state information that is specific to the application of the client is stored (persisted) using this name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

ExplorerBrowser can retrieve the properties stored in the property bag by calling function <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetviewstatepropertybag">SHGetViewStatePropertyBag</a>. 
 ExplorerBrowser writes to this property bag which is also stored (persisted) in the registry. Persistence occurs automatically when ExplorerBrowser destroys the current view, begins a navigation, or is destroyed. After any of these events, it writes information about the view state in case it has been modified by the user.

 If no properties have been stored, the default view state of the ExplorerBrowser is used. The default view state is the view state that the user has set for a particular location, or if the view state for a location has not been set (never modified by the user), then the default view state is based on the template for the file type (for example, documents, music and pictures) at the location. All Explorer windows use the same sequence to determine the default view state.