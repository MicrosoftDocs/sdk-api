---
UID: NF:bcrypt.BCryptGetProperty
title: BCryptGetProperty function (bcrypt.h)
description: Retrieves the value of a named property for a CNG object.
helpviewer_keywords: ["BCryptGetProperty","BCryptGetProperty function [Security]","bcrypt/BCryptGetProperty","security.bcryptgetproperty_func"]
old-location: security\bcryptgetproperty_func.htm
tech.root: security
ms.assetid: 5c62ca3a-843e-41a7-9340-41785fbb15f4
ms.date: 06/16/2025
ms.keywords: BCryptGetProperty, BCryptGetProperty function [Security], bcrypt/BCryptGetProperty, security.bcryptgetproperty_func
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
 - BCryptGetProperty
 - bcrypt/BCryptGetProperty
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
 - BCryptGetProperty
---

# BCryptGetProperty function

## -description

The **BCryptGetProperty** function retrieves the value of a named property for a CNG object.

## -parameters

### -param hObject [in]

A handle that represents the CNG object to obtain the property value for.

### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to retrieve. This can be one of the predefined [Cryptography Primitive Property Identifiers](/windows/win32/SecCNG/cng-property-identifiers) or a custom property identifier.

### -param pbOutput [out]

The address of a buffer that receives the property value. The *cbOutput* parameter contains the size of this buffer.

### -param cbOutput [in]

The size, in bytes, of the *pbOutput* buffer.

### -param pcbResult [out]

A pointer to a **ULONG** variable that receives the number of bytes that were copied to the *pbOutput* buffer. If the *pbOutput* parameter is `NULL`, this function will place the required size, in bytes, in the location pointed to by this parameter.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|--|--|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_BUFFER_TOO_SMALL** | The buffer size specified by the *cbOutput* parameter is not large enough to hold the property value. |
| **STATUS_INVALID_HANDLE** | The handle in the *hObject* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |
| **STATUS_NOT_SUPPORTED** | The property specified by the *pszProperty* parameter is not supported. |

## -remarks

To obtain the required size for a property, pass `NULL` for the *pbOutput* parameter. This function will place the required size, in bytes, in the value pointed to by the *pcbResult* parameter.

When using a supported algorithm provider, **BCryptGetProperty** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, any pointers passed to the **BCryptGetProperty** function must refer to nonpaged (or locked) memory. If the object specified in the *hObject* parameter is a handle, it must have been opened by using the **BCRYPT_PROV_DISPATCH** flag.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.
