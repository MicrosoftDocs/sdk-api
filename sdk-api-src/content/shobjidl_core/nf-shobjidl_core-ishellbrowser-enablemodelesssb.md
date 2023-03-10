---
UID: NF:shobjidl_core.IShellBrowser.EnableModelessSB
title: IShellBrowser::EnableModelessSB (shobjidl_core.h)
description: Tells Windows Explorer to enable or disable its modeless dialog boxes.
helpviewer_keywords: ["EnableModelessSB","EnableModelessSB method [Windows Shell]","EnableModelessSB method [Windows Shell]","IShellBrowser interface","IShellBrowser interface [Windows Shell]","EnableModelessSB method","IShellBrowser.EnableModelessSB","IShellBrowser::EnableModelessSB","_win32_IShellBrowser_EnableModelessSB","shell.IShellBrowser_EnableModelessSB","shobjidl_core/IShellBrowser::EnableModelessSB"]
old-location: shell\IShellBrowser_EnableModelessSB.htm
tech.root: shell
ms.assetid: 6bf39e3f-8b17-4307-ba57-7363c006c34b
ms.date: 12/05/2018
ms.keywords: EnableModelessSB, EnableModelessSB method [Windows Shell], EnableModelessSB method [Windows Shell],IShellBrowser interface, IShellBrowser interface [Windows Shell],EnableModelessSB method, IShellBrowser.EnableModelessSB, IShellBrowser::EnableModelessSB, _win32_IShellBrowser_EnableModelessSB, shell.IShellBrowser_EnableModelessSB, shobjidl_core/IShellBrowser::EnableModelessSB
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
 - IShellBrowser::EnableModelessSB
 - shobjidl_core/IShellBrowser::EnableModelessSB
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
 - IShellBrowser.EnableModelessSB
---

# IShellBrowser::EnableModelessSB


## -description

Tells Windows Explorer to enable or disable its modeless dialog boxes.

## -parameters

### -param fEnable

Type: <b>BOOL</b>

Specifies whether the modeless dialog boxes are to be enabled or disabled. If this parameter is nonzero, modeless dialog boxes are enabled. If this parameter is zero, modeless dialog boxes are disabled.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-enablemodeless">IOleInPlaceFrame::EnableModeless</a> method. Although the current version of Windows Explorer does not have any modeless dialog boxes, the view should call this method when it wants to disable or enable modeless dialog boxes associated with the Windows Explorer window.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>