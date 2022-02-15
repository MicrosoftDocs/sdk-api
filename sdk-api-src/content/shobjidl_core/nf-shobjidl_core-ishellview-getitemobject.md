---
UID: NF:shobjidl_core.IShellView.GetItemObject
title: IShellView::GetItemObject (shobjidl_core.h)
description: Gets an interface that refers to data presented in the view.
helpviewer_keywords: ["GetItemObject","GetItemObject method [Windows Shell]","GetItemObject method [Windows Shell]","IShellView interface","IShellView interface [Windows Shell]","GetItemObject method","IShellView.GetItemObject","IShellView::GetItemObject","_win32_IShellView_GetItemObject","shell.IShellView_GetItemObject","shobjidl_core/IShellView::GetItemObject"]
old-location: shell\IShellView_GetItemObject.htm
tech.root: shell
ms.assetid: 249ce8cc-6820-4f0a-a83a-2035e88d0d9c
ms.date: 12/05/2018
ms.keywords: GetItemObject, GetItemObject method [Windows Shell], GetItemObject method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],GetItemObject method, IShellView.GetItemObject, IShellView::GetItemObject, _win32_IShellView_GetItemObject, shell.IShellView_GetItemObject, shobjidl_core/IShellView::GetItemObject
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
 - IShellView::GetItemObject
 - shobjidl_core/IShellView::GetItemObject
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
 - IShellView.GetItemObject
---

# IShellView::GetItemObject


## -description

Gets an interface that refers to data presented in the view.

## -parameters

### -param uItem

Type: <b>UINT</b>

The constants that refer to an aspect of the view. This parameter can be any one of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">_SVGIO</a> constants.

### -param riid

Type: <b>REFIID</b>

The identifier of the COM interface being requested.

### -param ppv

Type: <b>LPVOID*</b>

The address that receives the interface pointer. If an error occurs, the pointer returned must be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Used by the common dialog boxes to retrieve the selected items from the view.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>