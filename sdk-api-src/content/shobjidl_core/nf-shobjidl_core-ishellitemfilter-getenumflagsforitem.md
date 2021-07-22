---
UID: NF:shobjidl_core.IShellItemFilter.GetEnumFlagsForItem
title: IShellItemFilter::GetEnumFlagsForItem (shobjidl_core.h)
description: Allows a client to specify which classes of objects in a Shell item should be enumerated for inclusion in the view.
helpviewer_keywords: ["GetEnumFlagsForItem","GetEnumFlagsForItem method [Windows Shell]","GetEnumFlagsForItem method [Windows Shell]","IShellItemFilter interface","IShellItemFilter interface [Windows Shell]","GetEnumFlagsForItem method","IShellItemFilter.GetEnumFlagsForItem","IShellItemFilter::GetEnumFlagsForItem","_shell_IShellItemFilter_GetEnumFlagsForItem","shell.IShellItemFilter_GetEnumFlagsForItem","shobjidl_core/IShellItemFilter::GetEnumFlagsForItem"]
old-location: shell\IShellItemFilter_GetEnumFlagsForItem.htm
tech.root: shell
ms.assetid: a84868ab-25c4-4cb7-84a1-aba0eff09b4a
ms.date: 12/05/2018
ms.keywords: GetEnumFlagsForItem, GetEnumFlagsForItem method [Windows Shell], GetEnumFlagsForItem method [Windows Shell],IShellItemFilter interface, IShellItemFilter interface [Windows Shell],GetEnumFlagsForItem method, IShellItemFilter.GetEnumFlagsForItem, IShellItemFilter::GetEnumFlagsForItem, _shell_IShellItemFilter_GetEnumFlagsForItem, shell.IShellItemFilter_GetEnumFlagsForItem, shobjidl_core/IShellItemFilter::GetEnumFlagsForItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemFilter::GetEnumFlagsForItem
 - shobjidl_core/IShellItemFilter::GetEnumFlagsForItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemFilter.GetEnumFlagsForItem
---

# IShellItemFilter::GetEnumFlagsForItem


## -description

Allows a client to specify which classes of objects in a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> should be enumerated for inclusion in the view.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> for which the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a> enum flags are to be retrieved.

### -param pgrfFlags [out]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a>*</b>

A pointer to the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a> enum flags for the given <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> that specifies which classes of objects to enumerate for inclusion in the view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a>



<a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a>