---
UID: NF:shlobj_core.IDockingWindowSite.GetBorderDW
title: IDockingWindowSite::GetBorderDW (shlobj_core.h)
description: Gets the border space allocated for the specified IDockingWindow object.
helpviewer_keywords: ["GetBorderDW","GetBorderDW method [Windows Shell]","GetBorderDW method [Windows Shell]","IDockingWindowSite interface","IDockingWindowSite interface [Windows Shell]","GetBorderDW method","IDockingWindowSite.GetBorderDW","IDockingWindowSite::GetBorderDW","_win32_IDockingWindowSite_GetBorderDW","shell.IDockingWindowSite_GetBorderDW","shlobj_core/IDockingWindowSite::GetBorderDW"]
old-location: shell\IDockingWindowSite_GetBorderDW.htm
tech.root: shell
ms.assetid: b1c30a49-8d87-4855-acc0-5f33eabe5e8a
ms.date: 12/05/2018
ms.keywords: GetBorderDW, GetBorderDW method [Windows Shell], GetBorderDW method [Windows Shell],IDockingWindowSite interface, IDockingWindowSite interface [Windows Shell],GetBorderDW method, IDockingWindowSite.GetBorderDW, IDockingWindowSite::GetBorderDW, _win32_IDockingWindowSite_GetBorderDW, shell.IDockingWindowSite_GetBorderDW, shlobj_core/IDockingWindowSite::GetBorderDW
req.header: shlobj_core.h
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
 - IDockingWindowSite::GetBorderDW
 - shlobj_core/IDockingWindowSite::GetBorderDW
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
 - IDockingWindowSite.GetBorderDW
---

# IDockingWindowSite::GetBorderDW


## -description

Gets the border space allocated for the specified <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object.

## -parameters

### -param punkObj [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object for which the border space is being requested.

### -param prcBorder [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a structure that, when this method returns successfully, receives the entire available border space for the browser. The docking window object should use this information to determine where to place itself. See the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw">IDockingWindow::ResizeBorderDW</a> method for more information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>