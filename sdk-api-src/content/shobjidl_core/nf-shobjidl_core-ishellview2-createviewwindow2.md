---
UID: NF:shobjidl_core.IShellView2.CreateViewWindow2
title: IShellView2::CreateViewWindow2 (shobjidl_core.h)
description: Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.
helpviewer_keywords: ["CreateViewWindow2","CreateViewWindow2 method [Windows Shell]","CreateViewWindow2 method [Windows Shell]","IShellView2 interface","IShellView2 interface [Windows Shell]","CreateViewWindow2 method","IShellView2.CreateViewWindow2","IShellView2::CreateViewWindow2","_win32_IShellView2_CreateViewWindow2","shell.IShellView2_CreateViewWindow2","shobjidl_core/IShellView2::CreateViewWindow2"]
old-location: shell\IShellView2_CreateViewWindow2.htm
tech.root: shell
ms.assetid: 3b829f5f-26ea-4987-be05-6725eeff5fed
ms.date: 12/05/2018
ms.keywords: CreateViewWindow2, CreateViewWindow2 method [Windows Shell], CreateViewWindow2 method [Windows Shell],IShellView2 interface, IShellView2 interface [Windows Shell],CreateViewWindow2 method, IShellView2.CreateViewWindow2, IShellView2::CreateViewWindow2, _win32_IShellView2_CreateViewWindow2, shell.IShellView2_CreateViewWindow2, shobjidl_core/IShellView2::CreateViewWindow2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView2::CreateViewWindow2
 - shobjidl_core/IShellView2::CreateViewWindow2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView2.CreateViewWindow2
---

# IShellView2::CreateViewWindow2


## -description

Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.

## -parameters

### -param lpParams

Type: <b>LPSV2CVW2_PARAMS</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sv2cvw2_params">SV2CVW2_PARAMS</a> structure that defines the new view window.

## -returns

Type: <b>HRESULT</b>

Returns a success code if successful, or a COM error code otherwise. Use the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to determine whether the operation succeeded or failed.

## -remarks

This method supersedes <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow">CreateViewWindow</a>. With <b>CreateViewWindow2</b>, developers are not restricted to the standard view modes provided by <b>CreateViewWindow</b>, but may also create their own. All view modes are now identified by their GUID.

The size of the structure, previous view window, folder settings, parent Shell browser, and view rectangle are passed into <b>IShellView2::CreateViewWindow2</b> in the first five members of <i>lpParams</i>. The method is responsible for creating the new window and passing back its window handle and the GUID of the view mode in the last two parameters. <b>IShellView2::CreateViewWindow2</b> should call the parent browser's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IShellBrowser::AddRef</a> method and store the interface pointer. It can be used for communication with the Windows Explorer window.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2">IShellView2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-getview">IShellView2::GetView</a>