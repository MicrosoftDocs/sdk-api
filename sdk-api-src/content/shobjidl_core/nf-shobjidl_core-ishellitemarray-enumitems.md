---
UID: NF:shobjidl_core.IShellItemArray.EnumItems
title: IShellItemArray::EnumItems (shobjidl_core.h)
description: Gets an enumerator of the items in the array.
helpviewer_keywords: ["EnumItems","EnumItems method [Windows Shell]","EnumItems method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","EnumItems method","IShellItemArray.EnumItems","IShellItemArray::EnumItems","_shell_IShellItemArray_EnumItems","shell.IShellItemArray_EnumItems","shobjidl_core/IShellItemArray::EnumItems"]
old-location: shell\IShellItemArray_EnumItems.htm
tech.root: shell
ms.assetid: c8ee210c-dab9-4678-9c62-d06677cbb395
ms.date: 12/05/2018
ms.keywords: EnumItems, EnumItems method [Windows Shell], EnumItems method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],EnumItems method, IShellItemArray.EnumItems, IShellItemArray::EnumItems, _shell_IShellItemArray_EnumItems, shell.IShellItemArray_EnumItems, shobjidl_core/IShellItemArray::EnumItems
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
 - IShellItemArray::EnumItems
 - shobjidl_core/IShellItemArray::EnumItems
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
 - IShellItemArray.EnumItems
---

# IShellItemArray::EnumItems


## -description

Gets an enumerator of the items in the array.

## -parameters

### -param ppenumShellItems [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>**</b>

When this method returns, contains an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> pointer that enumerates the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">shell items</a> that are in the array.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>