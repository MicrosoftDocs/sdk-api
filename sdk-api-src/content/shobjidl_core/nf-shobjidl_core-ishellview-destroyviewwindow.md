---
UID: NF:shobjidl_core.IShellView.DestroyViewWindow
title: IShellView::DestroyViewWindow (shobjidl_core.h)
description: Destroys the view window.
helpviewer_keywords: ["DestroyViewWindow","DestroyViewWindow method [Windows Shell]","DestroyViewWindow method [Windows Shell]","IShellView interface","IShellView interface [Windows Shell]","DestroyViewWindow method","IShellView.DestroyViewWindow","IShellView::DestroyViewWindow","_win32_IShellView_DestroyViewWindow","shell.IShellView_DestroyViewWindow","shobjidl_core/IShellView::DestroyViewWindow"]
old-location: shell\IShellView_DestroyViewWindow.htm
tech.root: shell
ms.assetid: b0dfc200-4438-4f11-a426-c82eeb9cc745
ms.date: 12/05/2018
ms.keywords: DestroyViewWindow, DestroyViewWindow method [Windows Shell], DestroyViewWindow method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],DestroyViewWindow method, IShellView.DestroyViewWindow, IShellView::DestroyViewWindow, _win32_IShellView_DestroyViewWindow, shell.IShellView_DestroyViewWindow, shobjidl_core/IShellView::DestroyViewWindow
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
 - IShellView::DestroyViewWindow
 - shobjidl_core/IShellView::DestroyViewWindow
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
 - IShellView.DestroyViewWindow
---

# IShellView::DestroyViewWindow


## -description

Destroys the view window.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

Windows Explorer calls this method when a folder window or Windows Explorer is being closed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Clean up all states that represent the view, including the window and any other associated resources.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
