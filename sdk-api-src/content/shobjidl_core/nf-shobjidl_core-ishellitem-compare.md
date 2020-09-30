---
UID: NF:shobjidl_core.IShellItem.Compare
title: IShellItem::Compare (shobjidl_core.h)
description: Compares two IShellItem objects.
helpviewer_keywords: ["Compare","Compare method [Windows Shell]","Compare method [Windows Shell]","IShellItem interface","IShellItem interface [Windows Shell]","Compare method","IShellItem.Compare","IShellItem::Compare","_win32_IShellItem_Compare","shell.IShellItem_Compare","shobjidl_core/IShellItem::Compare"]
old-location: shell\IShellItem_Compare.htm
tech.root: shell
ms.assetid: 737a93e0-2e27-466b-889c-04a25e52e883
ms.date: 12/05/2018
ms.keywords: Compare, Compare method [Windows Shell], Compare method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],Compare method, IShellItem.Compare, IShellItem::Compare, _win32_IShellItem_Compare, shell.IShellItem_Compare, shobjidl_core/IShellItem::Compare
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem::Compare
 - shobjidl_core/IShellItem::Compare
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
 - IShellItem.Compare
---

# IShellItem::Compare


## -description

Compares two <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> objects.

## -parameters

### -param psi

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object to compare with the existing <b>IShellItem</b> object.

### -param hint

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_sichintf">SICHINTF</a></b>

One of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_sichintf">SICHINTF</a> values that determines how to perform the comparison. See <b>SICHINTF</b> for the list of possible values for this parameter.

### -param piOrder

Type: <b>int*</b>

This parameter receives the result of the comparison. If the two items are the same this parameter equals zero; if they are different the parameter is nonzero.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the items are the same, S_FALSE if they are different, or an error value otherwise.

## -remarks

The data type used in the second parameter, SICHINTF, is defined as: 


```
typedef DWORD SICHINTF;
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>