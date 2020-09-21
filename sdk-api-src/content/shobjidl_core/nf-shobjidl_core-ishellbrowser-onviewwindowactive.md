---
UID: NF:shobjidl_core.IShellBrowser.OnViewWindowActive
title: IShellBrowser::OnViewWindowActive (shobjidl_core.h)
description: Called by the Shell view when the view window or one of its child windows gets the focus or becomes active.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","OnViewWindowActive method","IShellBrowser.OnViewWindowActive","IShellBrowser::OnViewWindowActive","OnViewWindowActive","OnViewWindowActive method [Windows Shell]","OnViewWindowActive method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_OnViewWindowActive","shell.IShellBrowser_OnViewWindowActive","shobjidl_core/IShellBrowser::OnViewWindowActive"]
old-location: shell\IShellBrowser_OnViewWindowActive.htm
tech.root: shell
ms.assetid: bd320262-f383-453b-9028-4e93f0b3761a
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],OnViewWindowActive method, IShellBrowser.OnViewWindowActive, IShellBrowser::OnViewWindowActive, OnViewWindowActive, OnViewWindowActive method [Windows Shell], OnViewWindowActive method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_OnViewWindowActive, shell.IShellBrowser_OnViewWindowActive, shobjidl_core/IShellBrowser::OnViewWindowActive
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
 - IShellBrowser::OnViewWindowActive
 - shobjidl_core/IShellBrowser::OnViewWindowActive
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
 - IShellBrowser.OnViewWindowActive
---

# IShellBrowser::OnViewWindowActive


## -description

Called by the Shell view when the view window or one of its child windows gets the focus or becomes active.

## -parameters

### -param pshv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

Address of the view object's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> pointer.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

The view must pass its <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> implementation to this routine, although the current version of Windows Explorer does not use this parameter.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The Shell view object must call this method before calling the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb">IShellBrowser::InsertMenusSB</a> method. This method will insert a different set of menu items depending on whether the view has the focus.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method informs the browser that the view is getting the focus (when the mouse is clicked on the view, for example).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>