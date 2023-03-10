---
UID: NF:shobjidl_core.IDockingWindow.CloseDW
title: IDockingWindow::CloseDW (shobjidl_core.h)
description: Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.
helpviewer_keywords: ["CloseDW","CloseDW method [Windows Shell]","CloseDW method [Windows Shell]","IDockingWindow interface","IDockingWindow interface [Windows Shell]","CloseDW method","IDockingWindow.CloseDW","IDockingWindow::CloseDW","_win32_IDockingWindow_CloseDW","shell.IDockingWindow_CloseDW","shobjidl_core/IDockingWindow::CloseDW"]
old-location: shell\IDockingWindow_CloseDW.htm
tech.root: shell
ms.assetid: 29e57436-cc8f-46e8-bc1a-b44bd803c4a8
ms.date: 12/05/2018
ms.keywords: CloseDW, CloseDW method [Windows Shell], CloseDW method [Windows Shell],IDockingWindow interface, IDockingWindow interface [Windows Shell],CloseDW method, IDockingWindow.CloseDW, IDockingWindow::CloseDW, _win32_IDockingWindow_CloseDW, shell.IDockingWindow_CloseDW, shobjidl_core/IDockingWindow::CloseDW
req.header: shobjidl_core.h
req.include-header: Shlobj.h
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
 - IDockingWindow::CloseDW
 - shobjidl_core/IDockingWindow::CloseDW
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
 - IDockingWindow.CloseDW
---

# IDockingWindow::CloseDW


## -description

Notifies the docking window object that it is about to be removed from the frame. The docking window object should save any persistent information at this time.

## -parameters

### -param dwReserved

Type: <b>DWORD</b>

Reserved. This parameter should always be zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>