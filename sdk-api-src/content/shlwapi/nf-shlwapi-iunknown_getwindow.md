---
UID: NF:shlwapi.IUnknown_GetWindow
title: IUnknown_GetWindow function (shlwapi.h)
description: Attempts to retrieve a window handle from a Component Object Model (COM) object by querying for various interfaces that have a GetWindow method.
helpviewer_keywords: ["IUnknown_GetWindow","IUnknown_GetWindow function [Windows Shell]","_win32_IUnknown_GetWindow","shell.IUnknown_GetWindow","shlwapi/IUnknown_GetWindow"]
old-location: shell\IUnknown_GetWindow.htm
tech.root: shell
ms.assetid: f8a6f61f-bea3-4049-89fb-c33ef00b327f
ms.date: 12/05/2018
ms.keywords: IUnknown_GetWindow, IUnknown_GetWindow function [Windows Shell], _win32_IUnknown_GetWindow, shell.IUnknown_GetWindow, shlwapi/IUnknown_GetWindow
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnknown_GetWindow
 - shlwapi/IUnknown_GetWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - IUnknown_GetWindow
---

# IUnknown_GetWindow function


## -description

Attempts to retrieve a window handle from a Component Object Model (COM) object by querying for various interfaces that have a <b>GetWindow</b> method.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the COM object from which this function will attempt to obtain a window handle.

### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to a HWND that, when this function returns successfully, receives the window handle. If a window handle was not obtained, this parameter is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if a window handle was successfully returned, or a COM error code otherwise. If no suitable interface was found, the function returns E_NOINTERFACE. Otherwise, the function returns the <b>HRESULT</b> returned by the corresponding interface's <b>GetWindow</b> method.

## -remarks

This function attempts to retrieve the window handle by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IOleWindow::GetWindow</a>, <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537095(v=vs.85)">IInternetSecurityMgrSite::GetWindow</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView::GetWindow</a>. It is possible that future versions of <b>IUnknown_GetWindow</b> may attempt additional interfaces.

<div class="alert"><b>Note</b>  The query for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> is theoretically unnecessary because <b>IShellView</b> derives from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. The function explicitly queries for this interface because some objects implement <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> incorrectly and fail to respond to a query for the base interface.</div>
<div> </div>