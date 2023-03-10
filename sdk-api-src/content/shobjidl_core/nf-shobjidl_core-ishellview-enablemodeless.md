---
UID: NF:shobjidl_core.IShellView.EnableModeless
title: IShellView::EnableModeless (shobjidl_core.h)
description: Enables or disables modeless dialog boxes. This method is not currently implemented.
helpviewer_keywords: ["EnableModeless","EnableModeless method [Windows Shell]","EnableModeless method [Windows Shell]","IShellView interface","IShellView interface [Windows Shell]","EnableModeless method","IShellView.EnableModeless","IShellView::EnableModeless","_win32_IShellView_EnableModeless","shell.IShellView_EnableModeless","shobjidl_core/IShellView::EnableModeless"]
old-location: shell\IShellView_EnableModeless.htm
tech.root: shell
ms.assetid: 5467f524-fa61-4919-bf64-268f9387b2f2
ms.date: 12/05/2018
ms.keywords: EnableModeless, EnableModeless method [Windows Shell], EnableModeless method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],EnableModeless method, IShellView.EnableModeless, IShellView::EnableModeless, _win32_IShellView_EnableModeless, shell.IShellView_EnableModeless, shobjidl_core/IShellView::EnableModeless
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
 - IShellView::EnableModeless
 - shobjidl_core/IShellView::EnableModeless
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
 - IShellView.EnableModeless
---

# IShellView::EnableModeless


## -description

Enables or disables modeless dialog boxes. This method is not currently implemented.

## -parameters

### -param fEnable

Type: <b>BOOL</b>

Nonzero to enable modeless dialog box windows or zero to disable them.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>