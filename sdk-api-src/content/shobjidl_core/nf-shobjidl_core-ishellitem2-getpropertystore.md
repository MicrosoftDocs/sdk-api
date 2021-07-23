---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStore
title: IShellItem2::GetPropertyStore (shobjidl_core.h)
description: Gets a property store object for specified property store flags.
helpviewer_keywords: ["GetPropertyStore","GetPropertyStore method [Windows Shell]","GetPropertyStore method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetPropertyStore method","IShellItem2.GetPropertyStore","IShellItem2::GetPropertyStore","_shell_IShellItem2_GetPropertyStore","shell.IShellItem2_GetPropertyStore","shobjidl_core/IShellItem2::GetPropertyStore"]
old-location: shell\IShellItem2_GetPropertyStore.htm
tech.root: shell
ms.assetid: 706b2551-a9b0-4368-babb-e54cea6d297e
ms.date: 12/05/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Shell], GetPropertyStore method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStore method, IShellItem2.GetPropertyStore, IShellItem2::GetPropertyStore, _shell_IShellItem2_GetPropertyStore, shell.IShellItem2_GetPropertyStore, shobjidl_core/IShellItem2::GetPropertyStore
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
 - IShellItem2::GetPropertyStore
 - shobjidl_core/IShellItem2::GetPropertyStore
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
 - IShellItem2.GetPropertyStore
---

# IShellItem2::GetPropertyStore


## -description

Gets a property store object for specified property store flags.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

The <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> constants that modify the property store object.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the object to be retrieved.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.</div>
<div> </div>