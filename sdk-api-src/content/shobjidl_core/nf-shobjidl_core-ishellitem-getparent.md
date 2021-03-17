---
UID: NF:shobjidl_core.IShellItem.GetParent
title: IShellItem::GetParent (shobjidl_core.h)
description: Gets the parent of an IShellItem object.
helpviewer_keywords: ["GetParent","GetParent method [Windows Shell]","GetParent method [Windows Shell]","IShellItem interface","IShellItem interface [Windows Shell]","GetParent method","IShellItem.GetParent","IShellItem::GetParent","_win32_IShellItem_GetParent","shell.IShellItem_GetParent","shobjidl_core/IShellItem::GetParent"]
old-location: shell\IShellItem_GetParent.htm
tech.root: shell
ms.assetid: d62123af-2ae2-40f2-8581-c95b18491f20
ms.date: 12/05/2018
ms.keywords: GetParent, GetParent method [Windows Shell], GetParent method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],GetParent method, IShellItem.GetParent, IShellItem::GetParent, _win32_IShellItem_GetParent, shell.IShellItem_GetParent, shobjidl_core/IShellItem::GetParent
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem::GetParent
 - shobjidl_core/IShellItem::GetParent
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
 - IShellItem.GetParent
---

# IShellItem::GetParent


## -description

Gets the parent of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object.

## -parameters

### -param ppsi

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to the parent of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>