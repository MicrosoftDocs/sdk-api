---
UID: NF:oaidl.IPropertyBag.Write
tech.root: com
title: IPropertyBag::Write
ms.date: 05/25/2021
targetos: Windows
description: Save the named property in a caller-initialized VARIANT.
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
 - IPropertyBag::Write
f1_keywords:
 - IPropertyBag::Write
 - oaidl/IPropertyBag::Write
dev_langs:
 - c++
---

## -description

Save the named property in a caller-initialized VARIANT.

## -parameters

### -param pszPropName

The address of a string containing the name of the property to write. This cannot be NULL.

### -param pVar

The address of the caller-initialized VARIANT that holds the property value to save. The caller owns this VARIANT, and is responsible for all of its allocations. That is, the property bag does not attempt to free data in the VARIANT.

## -returns

## -remarks

The **Write** method tells the property bag to save the property named with *pszPropName* by using the type and value in the caller-initialized VARIANT in *pVar*. In some cases, the caller might be telling the property bag to save another object, for example, when `pVar->vt` is VT_UNKNOWN. In such cases, the property bag queries this object pointer for a persistence interface, such as IPersistStream or IPersistPropertyBag, and has that object save its data as well. Usually this results in the property bag having some byte array for this object, which can be saved as encoded text, such as hexadecimal string, MIME, and so on. When the property bag is later used to reinitialize a control, the client that owns the property bag must re-create the object when the caller asks for it, initializing that object with the previously saved bits.

This allows efficient persistence operations for Binary Large Object (BLOB) properties, such as a picture, where the owner of the property bag tells the picture object (which is managed as a property in the control that is saved) to save to a specific location. This avoids potential extra copy operations that might be involved with other property-based persistence mechanisms.

E_NOTIMPL is not a valid return code, because any object that implements this interface must support the entire functionality of the interface.

## -see-also

