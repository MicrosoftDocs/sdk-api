---
UID: NF:shlobj.IDockingWindowFrame.RemoveToolbar
title: IDockingWindowFrame::RemoveToolbar (shlobj.h)
description: Removes the specified IDockingWindow from the toolbar frame.
helpviewer_keywords: ["DWFRF_DELETECONFIGDATA","DWFRF_NORMAL","IDockingWindowFrame interface [Windows Shell]","RemoveToolbar method","IDockingWindowFrame.RemoveToolbar","IDockingWindowFrame::RemoveToolbar","RemoveToolbar","RemoveToolbar method [Windows Shell]","RemoveToolbar method [Windows Shell]","IDockingWindowFrame interface","_win32_IDockingWindowFrame_RemoveToolbar","shell.IDockingWindowFrame_RemoveToolbar","shlobj/IDockingWindowFrame::RemoveToolbar"]
old-location: shell\IDockingWindowFrame_RemoveToolbar.htm
tech.root: shell
ms.assetid: 4ebc4561-a7fe-4fa4-ae2a-88030ede02e7
ms.date: 12/05/2018
ms.keywords: DWFRF_DELETECONFIGDATA, DWFRF_NORMAL, IDockingWindowFrame interface [Windows Shell],RemoveToolbar method, IDockingWindowFrame.RemoveToolbar, IDockingWindowFrame::RemoveToolbar, RemoveToolbar, RemoveToolbar method [Windows Shell], RemoveToolbar method [Windows Shell],IDockingWindowFrame interface, _win32_IDockingWindowFrame_RemoveToolbar, shell.IDockingWindowFrame_RemoveToolbar, shlobj/IDockingWindowFrame::RemoveToolbar
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
 - IDockingWindowFrame::RemoveToolbar
 - shlobj/IDockingWindowFrame::RemoveToolbar
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
 - IDockingWindowFrame.RemoveToolbar
---

# IDockingWindowFrame::RemoveToolbar


## -description

Removes the specified <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> from the toolbar frame.

## -parameters

### -param punkSrc [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object to be removed. The <a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a> implementation calls the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw">IDockingWindow::CloseDW</a> and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IDockingWindow::Release</a> methods.

### -param dwRemoveFlags

Type: <b>DWORD</b>

Option flags for removing the docking window object. This parameter can be one or more of the following values:



#### DWFRF_NORMAL (0x0000)

The default delete processing is performed.



#### DWFRF_DELETECONFIGDATA (0x0001)

In addition to deleting the toolbar, any configuration data is removed as well.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>