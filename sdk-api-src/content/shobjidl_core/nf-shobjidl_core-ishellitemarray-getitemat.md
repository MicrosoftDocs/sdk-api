---
UID: NF:shobjidl_core.IShellItemArray.GetItemAt
title: IShellItemArray::GetItemAt (shobjidl_core.h)
description: Gets the item at the given index in the IShellItemArray.
helpviewer_keywords: ["GetItemAt","GetItemAt method [Windows Shell]","GetItemAt method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","GetItemAt method","IShellItemArray.GetItemAt","IShellItemArray::GetItemAt","_shell_IShellItemArray_GetItemAt","shell.IShellItemArray_GetItemAt","shobjidl_core/IShellItemArray::GetItemAt"]
old-location: shell\IShellItemArray_GetItemAt.htm
tech.root: shell
ms.assetid: 58307102-1ae3-4249-81e0-25c1166500d0
ms.date: 12/05/2018
ms.keywords: GetItemAt, GetItemAt method [Windows Shell], GetItemAt method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetItemAt method, IShellItemArray.GetItemAt, IShellItemArray::GetItemAt, _shell_IShellItemArray_GetItemAt, shell.IShellItemArray_GetItemAt, shobjidl_core/IShellItemArray::GetItemAt
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
 - IShellItemArray::GetItemAt
 - shobjidl_core/IShellItemArray::GetItemAt
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
 - IShellItemArray.GetItemAt
---

# IShellItemArray::GetItemAt


## -description

Gets the item at the given index in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

## -parameters

### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> requested in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>

### -param ppsi [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When this method returns, contains the requested <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function returns E_FAIL if the requested index is out of bounds of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getcount">IShellItemArray::GetCount</a>