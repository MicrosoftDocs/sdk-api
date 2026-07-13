---
UID: NF:shobjidl_core.SHGetItemFromDataObject
title: SHGetItemFromDataObject function (shobjidl_core.h)
description: Creates an IShellItem or related object based on an item specified by an IDataObject.
helpviewer_keywords: ["SHGetItemFromDataObject","SHGetItemFromDataObject function [Windows Shell]","_shell_SHGetItemFromDataObject","shell.SHGetItemFromDataObject","shobjidl_core/SHGetItemFromDataObject"]
old-location: shell\SHGetItemFromDataObject.htm
tech.root: shell
ms.assetid: 1d7b9ffa-9980-4d68-85e4-7bab667be168
ms.date: 12/05/2018
ms.keywords: SHGetItemFromDataObject, SHGetItemFromDataObject function [Windows Shell], _shell_SHGetItemFromDataObject, shell.SHGetItemFromDataObject, shobjidl_core/SHGetItemFromDataObject
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetItemFromDataObject
 - shobjidl_core/SHGetItemFromDataObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetItemFromDataObject
---

# SHGetItemFromDataObject function


## -description

Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or related object based on an item specified by an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>.

## -parameters

### -param pdtobj [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the source <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> instance.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags">DATAOBJ_GET_ITEM_FLAGS</a></b>

One or more values from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags">DATAOBJ_GET_ITEM_FLAGS</a> enumeration to specify options regarding the target object. This value can be 0.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItem.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.