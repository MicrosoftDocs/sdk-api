---
UID: NF:shobjidl_core.IShellBrowser.GetControlWindow
title: IShellBrowser::GetControlWindow (shobjidl_core.h)
description: Gets the window handle to a browser control.
helpviewer_keywords: ["FCW_PROGRESS","FCW_STATUS","FCW_TOOLBAR","FCW_TREE","GetControlWindow","GetControlWindow method [Windows Shell]","GetControlWindow method [Windows Shell]","IShellBrowser interface","IShellBrowser interface [Windows Shell]","GetControlWindow method","IShellBrowser.GetControlWindow","IShellBrowser::GetControlWindow","_win32_IShellBrowser_GetControlWindow","shell.IShellBrowser_GetControlWindow","shobjidl_core/IShellBrowser::GetControlWindow"]
old-location: shell\IShellBrowser_GetControlWindow.htm
tech.root: shell
ms.assetid: 0ddcdafd-01f6-441c-9cc8-1ca9f1209e25
ms.date: 12/05/2018
ms.keywords: FCW_PROGRESS, FCW_STATUS, FCW_TOOLBAR, FCW_TREE, GetControlWindow, GetControlWindow method [Windows Shell], GetControlWindow method [Windows Shell],IShellBrowser interface, IShellBrowser interface [Windows Shell],GetControlWindow method, IShellBrowser.GetControlWindow, IShellBrowser::GetControlWindow, _win32_IShellBrowser_GetControlWindow, shell.IShellBrowser_GetControlWindow, shobjidl_core/IShellBrowser::GetControlWindow
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
 - IShellBrowser::GetControlWindow
 - shobjidl_core/IShellBrowser::GetControlWindow
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
 - IShellBrowser.GetControlWindow
---

# IShellBrowser::GetControlWindow


## -description

Gets the window handle to a browser control.

## -parameters

### -param id

Type: <b>UINT</b>

The control handle that is being requested. This parameter can be one of the following values: 



#### FCW_TOOLBAR

Retrieves the window handle to the browser's toolbar.



#### FCW_STATUS

Retrieves the window handle to the browser's status bar.



#### FCW_TREE

Retrieves the window handle to the browser's tree view.



#### FCW_PROGRESS

Retrieves the window handle to the browser's progress bar.

### -param phwnd

Type: <b>HWND*</b>

The address of the window handle to the Windows Explorer control.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

<b>GetControlWindow</b> is used so views can directly manipulate the browser's controls. <b>FCW_TREE</b> should be used only to determine if the tree is present.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
<b>GetControlWindow</b> is used to manipulate and test the state of the control windows. Do not send messages directly to these controls; instead, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg">IShellBrowser::SendControlMsg</a>. Be prepared for this method to return <b>NULL</b>. Later versions of Windows Explorer may not include a toolbar, status bar, or tree window.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<b>GetControlWindow</b> returns the window handle to these controls if they exist in your implementation.

See also <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>