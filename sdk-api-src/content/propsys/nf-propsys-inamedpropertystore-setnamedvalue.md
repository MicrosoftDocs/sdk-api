---
UID: NF:propsys.INamedPropertyStore.SetNamedValue
title: INamedPropertyStore::SetNamedValue (propsys.h)
description: Sets the value of a named property.
helpviewer_keywords: ["INamedPropertyStore interface [Windows Shell]","SetNamedValue method","INamedPropertyStore.SetNamedValue","INamedPropertyStore::SetNamedValue","SetNamedValue","SetNamedValue method [Windows Shell]","SetNamedValue method [Windows Shell]","INamedPropertyStore interface","_shell_INamedPropertyStore_SetNamedValue","propsys/INamedPropertyStore::SetNamedValue","shell.INamedPropertyStore_SetNamedValue"]
old-location: shell\INamedPropertyStore_SetNamedValue.htm
tech.root: shell
ms.assetid: e1ccf53f-3117-45c2-a0ff-94f1bb084414
ms.date: 12/05/2018
ms.keywords: INamedPropertyStore interface [Windows Shell],SetNamedValue method, INamedPropertyStore.SetNamedValue, INamedPropertyStore::SetNamedValue, SetNamedValue, SetNamedValue method [Windows Shell], SetNamedValue method [Windows Shell],INamedPropertyStore interface, _shell_INamedPropertyStore_SetNamedValue, propsys/INamedPropertyStore::SetNamedValue, shell.INamedPropertyStore_SetNamedValue
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - INamedPropertyStore::SetNamedValue
 - propsys/INamedPropertyStore::SetNamedValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - INamedPropertyStore.SetNamedValue
---

# INamedPropertyStore::SetNamedValue


## -description

Sets the value of a named property.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the property name, as a Unicode string, in the named property store.

### -param propvar [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the value to set for the property named in <i>pszName</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.