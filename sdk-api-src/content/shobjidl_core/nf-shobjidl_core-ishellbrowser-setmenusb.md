---
UID: NF:shobjidl_core.IShellBrowser.SetMenuSB
title: IShellBrowser::SetMenuSB (shobjidl_core.h)
description: Installs the composite menu in the view window.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","SetMenuSB method","IShellBrowser.SetMenuSB","IShellBrowser::SetMenuSB","SetMenuSB","SetMenuSB method [Windows Shell]","SetMenuSB method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_SetMenuSB","shell.IShellBrowser_SetMenuSB","shobjidl_core/IShellBrowser::SetMenuSB"]
old-location: shell\IShellBrowser_SetMenuSB.htm
tech.root: shell
ms.assetid: ae6fe864-7fa1-4c74-a27f-d428bdeccc3d
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],SetMenuSB method, IShellBrowser.SetMenuSB, IShellBrowser::SetMenuSB, SetMenuSB, SetMenuSB method [Windows Shell], SetMenuSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SetMenuSB, shell.IShellBrowser_SetMenuSB, shobjidl_core/IShellBrowser::SetMenuSB
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
 - IShellBrowser::SetMenuSB
 - shobjidl_core/IShellBrowser::SetMenuSB
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
 - IShellBrowser.SetMenuSB
---

# IShellBrowser::SetMenuSB


## -description

Installs the composite menu in the view window.

## -parameters

### -param hmenuShared

Type: <b>HMENU</b>

A handle to the composite menu constructed by calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb">IShellBrowser::InsertMenusSB</a> and the <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a> function.

### -param holemenuRes

Type: <b>HOLEMENU</b>

### -param hwndActiveObject

Type: <b>HWND</b>

The view's window handle.

## -returns

Type: <b>RESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a> method. However, Windows Explorer performs menu dispatch based on the menu item identifier.

The availability of specific menu items depends on whether the view has the focus. Accordingly, it is necessary to call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive">IShellBrowser::OnViewWindowActive</a> method whenever the view window (or one of its child windows) has the focus.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
The object calls <b>IShellBrowser_SetMenuSB</b> to ask the container to install the composite menu structure set up by calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb">IShellBrowser::InsertMenusSB</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A container's implementation of this method should call the <b>SetMenu</b> function.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>