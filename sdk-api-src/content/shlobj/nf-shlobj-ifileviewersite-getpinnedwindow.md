---
UID: NF:shlobj.IFileViewerSite.GetPinnedWindow
title: IFileViewerSite::GetPinnedWindow (shlobj.h)
description: Gets the handle to the current pinned window, if one exists.
helpviewer_keywords: ["GetPinnedWindow","GetPinnedWindow method [Windows Shell]","GetPinnedWindow method [Windows Shell]","IFileViewerSite interface","IFileViewerSite interface [Windows Shell]","GetPinnedWindow method","IFileViewerSite.GetPinnedWindow","IFileViewerSite::GetPinnedWindow","_win32_IFileViewerSite_GetPinnedWindow","shell.IFileViewerSite_GetPinnedWindow","shlobj/IFileViewerSite::GetPinnedWindow"]
old-location: shell\IFileViewerSite_GetPinnedWindow.htm
tech.root: shell
ms.assetid: ef5b4668-1e74-42c2-903e-8d4cf5e2f74e
ms.date: 12/05/2018
ms.keywords: GetPinnedWindow, GetPinnedWindow method [Windows Shell], GetPinnedWindow method [Windows Shell],IFileViewerSite interface, IFileViewerSite interface [Windows Shell],GetPinnedWindow method, IFileViewerSite.GetPinnedWindow, IFileViewerSite::GetPinnedWindow, _win32_IFileViewerSite_GetPinnedWindow, shell.IFileViewerSite_GetPinnedWindow, shlobj/IFileViewerSite::GetPinnedWindow
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileViewerSite::GetPinnedWindow
 - shlobj/IFileViewerSite::GetPinnedWindow
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
 - IFileViewerSite.GetPinnedWindow
---

# IFileViewerSite::GetPinnedWindow


## -description

Gets the handle to the current pinned window, if one exists.

## -parameters

### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the handle of the current pinned window or <b>NULL</b> if no pinned window exists.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite">IFileViewerSite</a>