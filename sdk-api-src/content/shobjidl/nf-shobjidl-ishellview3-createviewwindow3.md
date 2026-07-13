---
UID: NF:shobjidl.IShellView3.CreateViewWindow3
title: IShellView3::CreateViewWindow3 (shobjidl.h)
description: Requests the creation of a new Shell view window. The view can be either the right pane of Windows Explorer or the client window of a folder window. This method replaces CreateViewWindow2.
helpviewer_keywords: ["CreateViewWindow3","CreateViewWindow3 method [Windows Shell]","CreateViewWindow3 method [Windows Shell]","IShellView3 interface","IShellView3 interface [Windows Shell]","CreateViewWindow3 method","IShellView3.CreateViewWindow3","IShellView3::CreateViewWindow3","SV3CVW3_DEFAULT","SV3CVW3_FORCEFOLDERFLAGS","SV3CVW3_FORCEVIEWMODE","SV3CVW3_NONINTERACTIVE","_shell_IShellView3_CreateViewWindow3","shell.IShellView3_CreateViewWindow3","shobjidl/IShellView3::CreateViewWindow3"]
old-location: shell\IShellView3_CreateViewWindow3.htm
tech.root: shell
ms.assetid: d5790f31-922d-41cc-b9a7-0b809615ef1f
ms.date: 12/05/2018
ms.keywords: CreateViewWindow3, CreateViewWindow3 method [Windows Shell], CreateViewWindow3 method [Windows Shell],IShellView3 interface, IShellView3 interface [Windows Shell],CreateViewWindow3 method, IShellView3.CreateViewWindow3, IShellView3::CreateViewWindow3, SV3CVW3_DEFAULT, SV3CVW3_FORCEFOLDERFLAGS, SV3CVW3_FORCEVIEWMODE, SV3CVW3_NONINTERACTIVE, _shell_IShellView3_CreateViewWindow3, shell.IShellView3_CreateViewWindow3, shobjidl/IShellView3::CreateViewWindow3
req.header: shobjidl.h
req.include-header: 
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
 - IShellView3::CreateViewWindow3
 - shobjidl/IShellView3::CreateViewWindow3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IShellView3.CreateViewWindow3
---

# IShellView3::CreateViewWindow3


## -description

Requests the creation of a new Shell view window. The view can be either the right pane of Windows Explorer or the client window of a folder window. This method replaces <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2">CreateViewWindow2</a>.

## -parameters

### -param psbOwner [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> interface to provide namespace extension services.

### -param psvPrev [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface that represents the previous view in the Windows Explorer or folder window.

### -param dwViewFlags [in]

Type: <b>SV3CVW3_FLAGS</b>

Flags that specify details of the view being created.



#### SV3CVW3_DEFAULT

The default view.



#### SV3CVW3_NONINTERACTIVE

In the case of an error, the view should fail silently rather than displaying a UI.



#### SV3CVW3_FORCEVIEWMODE

The view mode set by <b>IShellView3::CreateViewWindow3</b> overrides the saved view state.



#### SV3CVW3_FORCEFOLDERFLAGS

Folder flags set by <b>IShellView3::CreateViewWindow3</b> override the saved view state.

### -param dwMask [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a></b>

A bitwise mask that specifies which folder options specified in <i>dwFlags</i> are to be used.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a></b>

A bitwise value that contains the folder options, as <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>, to use in the new view.

### -param fvMode [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a></b>

A bitwise value that contains the folder view mode options, as <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>, to use in the new view.

### -param pvid [in]

Type: <b>const SHELLVIEWID*</b>

A pointer to Shell view ID as a <b>GUID</b>.

### -param prcView [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that provides the dimensions of the view window.

### -param phwndView [out]

Type: <b>HWND*</b>

A value that receives a pointer to the handle of the new Shell view window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.