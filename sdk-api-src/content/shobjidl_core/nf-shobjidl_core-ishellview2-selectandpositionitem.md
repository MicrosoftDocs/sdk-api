---
UID: NF:shobjidl_core.IShellView2.SelectAndPositionItem
title: IShellView2::SelectAndPositionItem (shobjidl_core.h)
description: Selects and positions an item in a Shell View.
helpviewer_keywords: ["IShellView2 interface [Windows Shell]","SelectAndPositionItem method","IShellView2.SelectAndPositionItem","IShellView2::SelectAndPositionItem","SelectAndPositionItem","SelectAndPositionItem method [Windows Shell]","SelectAndPositionItem method [Windows Shell]","IShellView2 interface","_win32_IShellView2_SelectAndPositionItem","shell.IShellView2_SelectAndPositionItem","shobjidl_core/IShellView2::SelectAndPositionItem"]
old-location: shell\IShellView2_SelectAndPositionItem.htm
tech.root: shell
ms.assetid: d78f152b-2dcb-410d-821a-56601a3c57f2
ms.date: 12/05/2018
ms.keywords: IShellView2 interface [Windows Shell],SelectAndPositionItem method, IShellView2.SelectAndPositionItem, IShellView2::SelectAndPositionItem, SelectAndPositionItem, SelectAndPositionItem method [Windows Shell], SelectAndPositionItem method [Windows Shell],IShellView2 interface, _win32_IShellView2_SelectAndPositionItem, shell.IShellView2_SelectAndPositionItem, shobjidl_core/IShellView2::SelectAndPositionItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView2::SelectAndPositionItem
 - shobjidl_core/IShellView2::SelectAndPositionItem
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
 - IShellView2.SelectAndPositionItem
---

# IShellView2::SelectAndPositionItem


## -description

Selects and positions an item in a Shell View.

## -parameters

### -param pidlItem

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that uniquely identifies the item of interest.

### -param uFlags

Type: <b>UINT</b>

One of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svsif">_SVSIF</a> constants that specify the type of selection to apply.

### -param ppt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the new position.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.