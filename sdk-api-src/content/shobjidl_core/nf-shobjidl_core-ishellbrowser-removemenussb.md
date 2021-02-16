---
UID: NF:shobjidl_core.IShellBrowser.RemoveMenusSB
title: IShellBrowser::RemoveMenusSB (shobjidl_core.h)
description: Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","RemoveMenusSB method","IShellBrowser.RemoveMenusSB","IShellBrowser::RemoveMenusSB","RemoveMenusSB","RemoveMenusSB method [Windows Shell]","RemoveMenusSB method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_RemoveMenusSB","shell.IShellBrowser_RemoveMenusSB","shobjidl_core/IShellBrowser::RemoveMenusSB"]
old-location: shell\IShellBrowser_RemoveMenusSB.htm
tech.root: shell
ms.assetid: aa96ac59-62cd-4010-8a0f-b743527f61da
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],RemoveMenusSB method, IShellBrowser.RemoveMenusSB, IShellBrowser::RemoveMenusSB, RemoveMenusSB, RemoveMenusSB method [Windows Shell], RemoveMenusSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_RemoveMenusSB, shell.IShellBrowser_RemoveMenusSB, shobjidl_core/IShellBrowser::RemoveMenusSB
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
 - IShellBrowser::RemoveMenusSB
 - shobjidl_core/IShellBrowser::RemoveMenusSB
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
 - IShellBrowser.RemoveMenusSB
---

# IShellBrowser::RemoveMenusSB


## -description

Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.

## -parameters

### -param hmenuShared

Type: <b>HMENU</b>

A handle to the in-place composite menu that was constructed by calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb">IShellBrowser::InsertMenusSB</a> and the  <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a> function.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-removemenus">IOleInPlaceFrame::RemoveMenus</a> method.

The object should always permit the container to remove its menu elements from the composite menu before deactivating the shared user interface.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
The method is called by the object application while it is being UI-deactivated so the browser can remove its menus.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>