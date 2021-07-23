---
UID: NF:shlobj.IDockingWindowFrame.FindToolbar
title: IDockingWindowFrame::FindToolbar (shlobj.h)
description: Finds the specified IDockingWindow object in the toolbar frame and returns an interface pointer to it.
helpviewer_keywords: ["FindToolbar","FindToolbar method [Windows Shell]","FindToolbar method [Windows Shell]","IDockingWindowFrame interface","IDockingWindowFrame interface [Windows Shell]","FindToolbar method","IDockingWindowFrame.FindToolbar","IDockingWindowFrame::FindToolbar","_win32_IDockingWindowFrame_FindToolbar","shell.IDockingWindowFrame_FindToolbar","shlobj/IDockingWindowFrame::FindToolbar"]
old-location: shell\IDockingWindowFrame_FindToolbar.htm
tech.root: shell
ms.assetid: 9086f8ae-6a81-463d-9482-7a60701ab8de
ms.date: 12/05/2018
ms.keywords: FindToolbar, FindToolbar method [Windows Shell], FindToolbar method [Windows Shell],IDockingWindowFrame interface, IDockingWindowFrame interface [Windows Shell],FindToolbar method, IDockingWindowFrame.FindToolbar, IDockingWindowFrame::FindToolbar, _win32_IDockingWindowFrame_FindToolbar, shell.IDockingWindowFrame_FindToolbar, shlobj/IDockingWindowFrame::FindToolbar
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IDockingWindowFrame::FindToolbar
 - shlobj/IDockingWindowFrame::FindToolbar
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
 - IDockingWindowFrame.FindToolbar
---

# IDockingWindowFrame::FindToolbar


## -description

Finds the specified <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object in the toolbar frame and returns an interface pointer to it.

## -parameters

### -param pwszItem [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode, application-defined string used to identify the object. This is the same string that was passed to the <a href="/windows/desktop/api/shlobj/nf-shlobj-idockingwindowframe-addtoolbar">AddToolbar</a> method.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID. This is typically IID_IDockingWindow.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>. If an error occurs, this value receives a null pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>