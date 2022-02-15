---
UID: NF:shlobj.IFileViewerSite.SetPinnedWindow
title: IFileViewerSite::SetPinnedWindow (shlobj.h)
description: Sets the pinned window. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window instead of creating a new window.
helpviewer_keywords: ["IFileViewerSite interface [Windows Shell]","SetPinnedWindow method","IFileViewerSite.SetPinnedWindow","IFileViewerSite::SetPinnedWindow","SetPinnedWindow","SetPinnedWindow method [Windows Shell]","SetPinnedWindow method [Windows Shell]","IFileViewerSite interface","_win32_IFileViewerSite_SetPinnedWindow","shell.IFileViewerSite_SetPinnedWindow","shlobj/IFileViewerSite::SetPinnedWindow"]
old-location: shell\IFileViewerSite_SetPinnedWindow.htm
tech.root: shell
ms.assetid: 7c2bcb76-84aa-404e-9e0a-9ee966b6c91e
ms.date: 12/05/2018
ms.keywords: IFileViewerSite interface [Windows Shell],SetPinnedWindow method, IFileViewerSite.SetPinnedWindow, IFileViewerSite::SetPinnedWindow, SetPinnedWindow, SetPinnedWindow method [Windows Shell], SetPinnedWindow method [Windows Shell],IFileViewerSite interface, _win32_IFileViewerSite_SetPinnedWindow, shell.IFileViewerSite_SetPinnedWindow, shlobj/IFileViewerSite::SetPinnedWindow
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
 - IFileViewerSite::SetPinnedWindow
 - shlobj/IFileViewerSite::SetPinnedWindow
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
 - IFileViewerSite.SetPinnedWindow
---

# IFileViewerSite::SetPinnedWindow


## -description

Sets the pinned window. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window instead of creating a new window.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the new pinned window or <b>NULL</b> if there is to be no pinned window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite">IFileViewerSite</a>