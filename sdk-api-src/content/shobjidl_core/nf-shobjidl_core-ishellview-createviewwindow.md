---
UID: NF:shobjidl_core.IShellView.CreateViewWindow
title: IShellView::CreateViewWindow (shobjidl_core.h)
description: Creates a view window. This can be either the right pane of Windows Explorer or the client window of a folder window.
helpviewer_keywords: ["CreateViewWindow","CreateViewWindow method [Windows Shell]","CreateViewWindow method [Windows Shell]","IShellView interface","IShellView interface [Windows Shell]","CreateViewWindow method","IShellView.CreateViewWindow","IShellView::CreateViewWindow","_win32_IShellView_CreateViewWindow","shell.IShellView_CreateViewWindow","shobjidl_core/IShellView::CreateViewWindow"]
old-location: shell\IShellView_CreateViewWindow.htm
tech.root: shell
ms.assetid: 62d71bca-d2cb-4668-b0bf-2e53756f2cd9
ms.date: 12/05/2018
ms.keywords: CreateViewWindow, CreateViewWindow method [Windows Shell], CreateViewWindow method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],CreateViewWindow method, IShellView.CreateViewWindow, IShellView::CreateViewWindow, _win32_IShellView_CreateViewWindow, shell.IShellView_CreateViewWindow, shobjidl_core/IShellView::CreateViewWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView::CreateViewWindow
 - shobjidl_core/IShellView::CreateViewWindow
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
 - IShellView.CreateViewWindow
---

# IShellView::CreateViewWindow


## -description

Creates a view window. This can be either the right pane of Windows Explorer or the client window of a folder window.

## -parameters

### -param psvPrevious [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

The address of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface of the view window being exited. Views can use this parameter to communicate with a previous view of the same implementation. This interface can be used to optimize browsing between like views. This pointer may be <b>NULL</b>.

### -param pfs [in]

Type: <b>LPCFOLDERSETTINGS</b>

The address of a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure. The view should use this when creating its view.

### -param psb [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>*</b>

The address of the current instance of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> interface. The view should call this interface's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and keep the interface pointer to allow communication with the Windows Explorer window.

### -param prcView [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The dimensions of the new view, in client coordinates.

### -param phWnd [out]

Type: <b>HWND*</b>

The address of the window handle being created.

## -returns

Type: <b>HRESULT</b>

Returns a success code if successful, or a COM error code otherwise. Use the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to determine whether the operation succeeded or failed.

## -remarks

<h3><a id="Notes_to_Calling_applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling applications</h3>
Call this method when the view needs to be created.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Create your view window and restore any persistent state by calling the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream">GetViewStateStream</a> method. Store the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> pointer for further use.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>