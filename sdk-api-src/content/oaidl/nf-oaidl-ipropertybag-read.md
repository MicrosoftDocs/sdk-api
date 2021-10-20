---
UID: NF:oaidl.IPropertyBag.Read
tech.root: com
title: IPropertyBag::Read
ms.date: 05/25/2021
targetos: Windows
description: Reads the named property into a caller-initialized VARIANT.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: oaidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IPropertyBag::Read
f1_keywords:
 - IPropertyBag::Read
 - oaidl/IPropertyBag::Read
dev_langs:
 - c++
---

## -description

Reads the named property into a caller-initialized VARIANT.

## -parameters

### -param pszPropName

The address of the name of the property to read. This cannot be NULL.

### -param pVar

The address of the caller-initialized VARIANT that receives the property value on output. The function sets the type field and the value field in the VARIANT before it returns. If the caller initialized the `pVar->vt` field on entry, the property bag attempts to change its corresponding value to this type. If the caller sets `pVar->vt` to VT_EMPTY, the property bag can use whatever type is convenient.

### -param pErrorLog

The address of the caller's error log in which the property bag stores any errors that occur during reads. This can be NULL; in which case, the caller does not receive errors.

## -returns

An HRESULT

## -remarks

The **Read** method tells the property bag to read the property named in *pszPropName* to the caller-initialized VARIANT in *pVar*. Errors are logged in the error log that is pointed to by *pErrorLog*. When `pVar->vt` specifies another object pointer (VT_UNKNOWN), the property bag is responsible for creating and initializing the object described by *pszPropName*.

E_NOTIMPL is not a valid return code, because any object that implements this interface must support the entire functionality of the interface.

## -see-also

