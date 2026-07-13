---
UID: NF:wtsapi32.WTSCloudAuthConvertAssertionToSerializedUserCredential
tech.root: TermServ
title: WTSCloudAuthConvertAssertionToSerializedUserCredential
ms.date: 09/25/2025
targetos: Windows
description: Validates the assertion and computes the serialized credential from the assertion.
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
 - WTSCloudAuthConvertAssertionToSerializedUserCredential
f1_keywords:
 - WTSCloudAuthConvertAssertionToSerializedUserCredential
 - wtsapi32/WTSCloudAuthConvertAssertionToSerializedUserCredential
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthConvertAssertionToSerializedUserCredential
---

## -description

Validates the assertion and computes the serialized credential from the [assertion](/openspecs/windows_protocols/ms-rdpbcgr/ba819b6b-257a-466f-b8e5-f262d78677f7).

## -parameters

### -param cloudAuthHandle [in]

The cloud authentication handle obtained by calling [WTSCloudAuthOpen](./nf-wtsapi32-wtscloudauthopen.md).

### -param assertion [in]

A pointer to the assertion.

### -param assertionLength [in]

The size of the assertion string, in bytes.

### -param resourceId [in]

The expected identifier of the Resource App registered in Entra ID. This is used to ensure that the assertion targets the expected Resource App.

### -param userCredential [out]

Receives a pointer to an instance of `WTS_SERIALIZED_USER_CREDENTIAL` containing the serialized credential if the function succeeds. To free the allocated memory, call the `WTSFreeMemoryEx` function and pass `WTSTypeSerializedUserCredential` for the `WTSTypeClass` parameter.

## -returns

If the function succeeds, the return value is a nonzero value. If the function fails, the return value is zero. To get extended error information, call the [`GetLastError`](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

| Error Code | Description |
|---|---------------------------------|
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_APNONCE_INVALID) | The server nonce has expired. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_BAD_DEVICE_ACCESS_TOKEN_FORMAT) | The format of the access token is invalid. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_ASSERTION_MALFORMED) | The format of the assertion is invalid. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_INVALID_TENANT) | The Entra ID tenant specified in the server nonce or the assertion is invalid. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_INVALID_DEVICE) | The target device specified in the server nonce or the assertion is invalid. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_INVALID_ACCESS_TOKEN) | The access token is invalid. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_INVALID_BINDING_KEY_ID) | The binding key specified in the assertion does not match the binding key specified in the access token. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_CANT_FIND_ROOT_CERT) | The root certificate associated with the access token's signature cannot be found. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_ASSERTION_INVALID) | The resource URL in the assertion does not match the audience specified in the access token. |
| HRESULT_FROM_NT(STATUS_AAD_CLOUDAP_E_CALLER_MISMATCH) | The specified resource ID does not match the audience specified in the access token. |

The STATUS_AAD_CLOUDAP_E_* error codes are defined in winnt.h and ntstatus.h.

## -remarks

The client constructs the assertion, and the protocol is responsible for transporting the assertion to the server. The output serialized credentials can be used in `WTSCloudAuthNetworkLogonWithSerializedCredentials` to perform a network logon and additional authorization. Later, they can also be used in `IWRdsProtocolConnection2::GetSerializedUserCredentials` where a protocol can provide serialized credentials to the Remote Desktop Services service which performs an interactive logon on their behalf.

## -see-also

