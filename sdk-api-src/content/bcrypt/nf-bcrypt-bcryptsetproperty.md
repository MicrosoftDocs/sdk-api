---
UID: NF:bcrypt.BCryptSetProperty
title: BCryptSetProperty function (bcrypt.h)
description: Sets the value of a named property for a CNG object.
helpviewer_keywords: ["BCryptSetProperty","BCryptSetProperty function [Security]","bcrypt/BCryptSetProperty","security.bcryptsetproperty_func"]
old-location: security\bcryptsetproperty_func.htm
tech.root: security
ms.assetid: 687f3410-d28b-4ce2-a2a1-c564f757c668
ms.date: 12/05/2018
ms.keywords: BCryptSetProperty, BCryptSetProperty function [Security], bcrypt/BCryptSetProperty, security.bcryptsetproperty_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptSetProperty
 - bcrypt/BCryptSetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptSetProperty
---

# BCryptSetProperty function


## -description

The **BCryptSetProperty** function sets the value of a named property for a CNG object.

## -parameters

### -param hObject [in, out]

A handle that represents the CNG object to set the property value for.

### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to set. This can be one of the predefined [Cryptography Primitive Property Identifiers](/windows/win32/SecCNG/cng-property-identifiers) or a custom property identifier.

### -param pbInput [in]

The address of a buffer that contains the new property value. The *cbInput* parameter contains the size of this buffer.

### -param cbInput [in]

The size, in bytes, of the *pbInput* buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:


| Return code | Description |
|--|--|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_HANDLE** | The handle in the *hObject* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |
| **STATUS_NOT_SUPPORTED** | The named property specified by the *pszProperty* parameter is not supported or is read-only. |

## -remarks

When using a supported algorithm provider, **BCryptSetProperty** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, any pointers passed to **BCryptSetProperty** must refer to nonpaged (or locked) memory. If the object specified in the *hObject* parameter is a handle, it must have been opened by using the **BCRYPT_PROV_DISPATCH** flag.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

When [generating keys](nf-bcrypt-bcryptgeneratekeypair.md) for ML-DSA and ML-KEM, the **BCRYPT_PARAMETER_SET_NAME** property must be set on the key handle, before the key can be [finalized](nf-bcrypt-bcryptfinalizekeypair.md).

When setting the value for the property *BCRYPT_CHAINING_MODE*, the *pbInput* parameter is unbounded by *cbInput*. The caller needs to ensure a valid null-terminated Unicode string is provided.

## -see-also

[Cryptography Primitive Property Identifiers](/windows/win32/SecCNG/cng-property-identifiers)
