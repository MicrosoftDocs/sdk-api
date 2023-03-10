---
UID: NS:shobjidl_core._SV2CVW2_PARAMS
title: SV2CVW2_PARAMS (shobjidl_core.h)
description: Holds the parameters for the IShellView2::CreateViewWindow2 method.
helpviewer_keywords: ["*LPSV2CVW2_PARAMS","LPSV2CVW2_PARAMS","LPSV2CVW2_PARAMS structure pointer [Windows Shell]","SV2CVW2_PARAMS","SV2CVW2_PARAMS structure [Windows Shell]","_SV2CVW2_PARAMS","_win32_SV2CVW2_PARAMS","shell.SV2CVW2_PARAMS","shobjidl_core/LPSV2CVW2_PARAMS","shobjidl_core/SV2CVW2_PARAMS"]
old-location: shell\SV2CVW2_PARAMS.htm
tech.root: shell
ms.assetid: 7e165654-74ea-4d8b-81b7-11257f87af53
ms.date: 12/05/2018
ms.keywords: '*LPSV2CVW2_PARAMS, LPSV2CVW2_PARAMS, LPSV2CVW2_PARAMS structure pointer [Windows Shell], SV2CVW2_PARAMS, SV2CVW2_PARAMS structure [Windows Shell], _SV2CVW2_PARAMS, _win32_SV2CVW2_PARAMS, shell.SV2CVW2_PARAMS, shobjidl_core/LPSV2CVW2_PARAMS, shobjidl_core/SV2CVW2_PARAMS'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SV2CVW2_PARAMS, *LPSV2CVW2_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SV2CVW2_PARAMS
 - shobjidl_core/_SV2CVW2_PARAMS
 - LPSV2CVW2_PARAMS
 - shobjidl_core/LPSV2CVW2_PARAMS
 - SV2CVW2_PARAMS
 - shobjidl_core/SV2CVW2_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SV2CVW2_PARAMS
---

# SV2CVW2_PARAMS structure


## -description

Holds the parameters for the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2">IShellView2::CreateViewWindow2</a> method.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure.

### -field psvPrev

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface of the previous view. A Shell view can use this parameter to communicate with a previous view with the same implementation. It can also be used to optimize browsing between like views. This parameter may be <b>NULL</b>.

### -field pfs

Type: <b>LPFOLDERSETTINGS</b>

A <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure with information needed to create the view.

### -field psbOwner

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>*</b>

A pointer to the current instance of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> interface of the parent Shell browser. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2">IShellView2::CreateViewWindow2</a> should call this interface's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and store the interface pointer. It can be used for communication with the Windows Explorer window.

### -field prcView

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A <b>RECT</b> structure that defines the view's display area.

### -field pvid

Type: <b>const SHELLVIEWID*</b>

A pointer to a view ID. The view ID can be one of the Windows-defined VIDs or a custom, view-defined VID. This value takes precedence over the view mode designated in the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure pointed to by <b>pfs</b>.

### -field hwndView

Type: <b>HWND</b>

A window handle to the new Shell view.