---
UID: NF:propsys.INamedPropertyStore.GetNamedValue
title: INamedPropertyStore::GetNamedValue (propsys.h)
description: Gets the value of a named property from the named property store.
helpviewer_keywords: ["GetNamedValue","GetNamedValue method [Windows Shell]","GetNamedValue method [Windows Shell]","INamedPropertyStore interface","INamedPropertyStore interface [Windows Shell]","GetNamedValue method","INamedPropertyStore.GetNamedValue","INamedPropertyStore::GetNamedValue","_shell_INamedPropertyStore_GetNamedValue","propsys/INamedPropertyStore::GetNamedValue","shell.INamedPropertyStore_GetNamedValue"]
old-location: shell\INamedPropertyStore_GetNamedValue.htm
tech.root: shell
ms.assetid: d62fcacd-7af5-4618-9b76-bebb001bb827
ms.date: 12/05/2018
ms.keywords: GetNamedValue, GetNamedValue method [Windows Shell], GetNamedValue method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNamedValue method, INamedPropertyStore.GetNamedValue, INamedPropertyStore::GetNamedValue, _shell_INamedPropertyStore_GetNamedValue, propsys/INamedPropertyStore::GetNamedValue, shell.INamedPropertyStore_GetNamedValue
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
 - INamedPropertyStore::GetNamedValue
 - propsys/INamedPropertyStore::GetNamedValue
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
 - INamedPropertyStore.GetNamedValue
---

# INamedPropertyStore::GetNamedValue


## -description

Gets the value of a named property from the named property store.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the property name, as a Unicode string, of the property in the named property store.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that holds the property's value.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
                
                    

If the property named in <i>pszName</i> is not found in the property store, this method returns S_OK and the <i>pv</i> member is set to VT_EMPTY.