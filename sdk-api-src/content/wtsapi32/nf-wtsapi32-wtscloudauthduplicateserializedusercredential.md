---
UID: NF:wtsapi32.WTSCloudAuthDuplicateSerializedUserCredential
tech.root: TermServ
title: WTSCloudAuthDuplicateSerializedUserCredential
ms.date: 09/25/2025
targetos: Windows
description: Duplicates an instance of WTS_SERIALIZED_USER_CREDENTIAL.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtsapi32.dll
api_name:
 - WTSCloudAuthDuplicateSerializedUserCredential
f1_keywords:
 - WTSCloudAuthDuplicateSerializedUserCredential
 - wtsapi32/WTSCloudAuthDuplicateSerializedUserCredential
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthDuplicateSerializedUserCredential
---

## -description

Duplicates an instance of *[WTS_SERIALIZED_USER_CREDENTIAL](/windows/win32/api/wtsapi32/ns-wtsapi32-wts_serialized_user_credential)*.

## Syntax

```cpp
BOOL WINAPI WTSCloudAuthDuplicateSerializedUserCredential(
  [in] const WTS_SERIALIZED_USER_CREDENTIAL* userCredential,
  [out] WTS_SERIALIZED_USER_CREDENTIAL** duplicatedUserCredential
);
```

## -parameters

### -param userCredential [in]

The user credential obtained by calling *[WTSCloudAuthConvertAssertionToSerializedUserCredential](./nf-wtsapi32-wtscloudauthconvertassertiontoserializedusercredential.md)*.

### -param duplicatedUserCredential [out]

Receives a pointer to the duplicated instance of *WTS_SERIALIZED_USER_CREDENTIAL*. To free the allocated memory, call the *[WTSFreeMemoryEx](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsfreememoryexw)* function and pass *WTSTypeSerializedUserCredential* for the *WTSTypeClass* parameter.

## -returns

If the function succeeds, the return value is a nonzero value.
If the function fails, the return value is zero. To get extended error information, call the [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

## -see-also

