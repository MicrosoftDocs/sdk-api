---
UID: NF:shobjidl_core.IShellItem.GetDisplayName
title: IShellItem::GetDisplayName (shobjidl_core.h)
description: Gets the display name of the IShellItem object.
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [Windows Shell]","GetDisplayName method [Windows Shell]","IShellItem interface","IShellItem interface [Windows Shell]","GetDisplayName method","IShellItem.GetDisplayName","IShellItem::GetDisplayName","_win32_IShellItem_GetDisplayName","shell.IShellItem_GetDisplayName","shobjidl_core/IShellItem::GetDisplayName"]
old-location: shell\IShellItem_GetDisplayName.htm
tech.root: shell
ms.assetid: 9b159be9-3797-4c8b-90f8-9d3b3a3afb71
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Windows Shell], GetDisplayName method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],GetDisplayName method, IShellItem.GetDisplayName, IShellItem::GetDisplayName, _win32_IShellItem_GetDisplayName, shell.IShellItem_GetDisplayName, shobjidl_core/IShellItem::GetDisplayName
req.header: shobjidl_core.h
req.include-header: Shlguid.h
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem::GetDisplayName
 - shobjidl_core/IShellItem::GetDisplayName
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
 - IShellItem.GetDisplayName
---

# IShellItem::GetDisplayName


## -description

Gets the display name of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object.

## -parameters

### -param sigdnName [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN</a> values that indicates how the name should look.

### -param ppszName [out]

Type: <b>LPWSTR*</b>

A value that, when this function returns successfully, receives the address of a pointer to the retrieved display name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is the responsibility of the caller to free the string pointed to by <i>ppszName</i> when it is no longer needed. Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> on *<i>ppszName</i> to free the memory.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>