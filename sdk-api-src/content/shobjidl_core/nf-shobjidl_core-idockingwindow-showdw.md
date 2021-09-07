---
UID: NF:shobjidl_core.IDockingWindow.ShowDW
title: IDockingWindow::ShowDW (shobjidl_core.h)
description: Instructs the docking window object to show or hide itself.
helpviewer_keywords: ["IDockingWindow interface [Windows Shell]","ShowDW method","IDockingWindow.ShowDW","IDockingWindow::ShowDW","ShowDW","ShowDW method [Windows Shell]","ShowDW method [Windows Shell]","IDockingWindow interface","_win32_IDockingWindow_ShowDW","shell.IDockingWindow_ShowDW","shobjidl_core/IDockingWindow::ShowDW"]
old-location: shell\IDockingWindow_ShowDW.htm
tech.root: shell
ms.assetid: c33031d4-f9f4-4210-93be-963e5f299408
ms.date: 12/05/2018
ms.keywords: IDockingWindow interface [Windows Shell],ShowDW method, IDockingWindow.ShowDW, IDockingWindow::ShowDW, ShowDW, ShowDW method [Windows Shell], ShowDW method [Windows Shell],IDockingWindow interface, _win32_IDockingWindow_ShowDW, shell.IDockingWindow_ShowDW, shobjidl_core/IDockingWindow::ShowDW
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
 - IDockingWindow::ShowDW
 - shobjidl_core/IDockingWindow::ShowDW
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
 - IDockingWindow.ShowDW
---

# IDockingWindow::ShowDW


## -description

Instructs the docking window object to show or hide itself.

## -parameters

### -param fShow

Type: <b>BOOL</b>

<b>TRUE</b> if the docking window object should show its window. <b>FALSE</b> if the docking window object should hide its window and return its border space by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-setborderspacedw">SetBorderSpaceDW</a> with zero values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>