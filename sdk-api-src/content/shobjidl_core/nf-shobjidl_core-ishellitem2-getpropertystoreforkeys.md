---
UID: NF:shobjidl_core.IShellItem2.GetPropertyStoreForKeys
title: IShellItem2::GetPropertyStoreForKeys (shobjidl_core.h)
description: Gets property store object for specified property keys.
helpviewer_keywords: ["GetPropertyStoreForKeys","GetPropertyStoreForKeys method [Windows Shell]","GetPropertyStoreForKeys method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetPropertyStoreForKeys method","IShellItem2.GetPropertyStoreForKeys","IShellItem2::GetPropertyStoreForKeys","_shell_IShellItem2_GetPropertyStoreForKeys","shell.IShellItem2_GetPropertyStoreForKeys","shobjidl_core/IShellItem2::GetPropertyStoreForKeys"]
old-location: shell\IShellItem2_GetPropertyStoreForKeys.htm
tech.root: shell
ms.assetid: 2d32ece8-4a68-4bf2-a1ee-bd94a2aa6fbd
ms.date: 12/05/2018
ms.keywords: GetPropertyStoreForKeys, GetPropertyStoreForKeys method [Windows Shell], GetPropertyStoreForKeys method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyStoreForKeys method, IShellItem2.GetPropertyStoreForKeys, IShellItem2::GetPropertyStoreForKeys, _shell_IShellItem2_GetPropertyStoreForKeys, shell.IShellItem2_GetPropertyStoreForKeys, shobjidl_core/IShellItem2::GetPropertyStoreForKeys
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
 - IShellItem2::GetPropertyStoreForKeys
 - shobjidl_core/IShellItem2::GetPropertyStoreForKeys
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
 - IShellItem2.GetPropertyStoreForKeys
---

# IShellItem2::GetPropertyStoreForKeys


## -description

Gets property store object for specified property keys.

## -parameters

### -param rgKeys [in]

Type: <b>const <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures. Each structure contains a unique identifier for each property used in creating the property store.

### -param cKeys [in]

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures in the array pointed to by <i>rgKeys</i>.

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

<div class="alert"><b>Note</b>  When this method is called on a property store for a file, that file is held open for the lifetime of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.
      </div>
<div> </div>