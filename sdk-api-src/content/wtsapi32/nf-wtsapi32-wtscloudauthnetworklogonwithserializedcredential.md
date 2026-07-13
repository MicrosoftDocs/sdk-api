---
UID: NF:wtsapi32.WTSCloudAuthNetworkLogonWithSerializedCredential
tech.root: TermServ
title: WTSCloudAuthNetworkLogonWithSerializedCredential
ms.date: 09/25/2025
targetos: Windows
description: Performs a network logon using the provided serialized credentials.
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
 - WTSCloudAuthNetworkLogonWithSerializedCredential
f1_keywords:
 - WTSCloudAuthNetworkLogonWithSerializedCredential
 - wtsapi32/WTSCloudAuthNetworkLogonWithSerializedCredential
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthNetworkLogonWithSerializedCredential
---

## -description

Performs a network logon using the provided serialized credentials.

## -parameters

### -param cloudAuthHandle [in]

The cloud authentication handle obtained by calling [`WTSCloudAuthOpen`](./nf-wtsapi32-wtscloudauthopen.md).

### -param userCredential [in]

The serialized credential obtained by calling [`WTSCloudAuthConvertAssertionToSerializedCredential`](./nf-wtsapi32-wtscloudauthconvertassertiontoserializedusercredential.md).

### -param token [out]

Receives a handle that represents the user token if the function succeeds. Use [`CloseHandle`](/windows/win32/api/handleapi/nf-handleapi-closehandle) to close the handle.

## -returns

If the function succeeds, the return value is a nonzero value. If the function fails, the return value is zero. To get extended error information, call the [`GetLastError`](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

The user token handle can be used to perform additional checks by, for instance, calling [`CheckTokenMembership`](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership).

## -see-also
