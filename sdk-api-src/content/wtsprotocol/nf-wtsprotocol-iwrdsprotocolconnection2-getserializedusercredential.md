---
UID: NF:wtsprotocol.IWRdsProtocolConnection2.GetSerializedUserCredential
tech.root: TermServ
title: IWRdsProtocolConnection2::GetSerializedUserCredential
ms.date: 09/25/2025
targetos: Windows
description: Returns a serialized user credential.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsprotocol.h
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
 - COM
api_location:
 - wtsprotocol.dll
api_name:
 - IWRdsProtocolConnection2::GetSerializedUserCredential
f1_keywords:
 - IWRdsProtocolConnection2::GetSerializedUserCredential
 - wtsprotocol/IWRdsProtocolConnection2::GetSerializedUserCredential
dev_langs:
 - c++
helpviewer_keywords:
 - GetSerializedUserCredential
---

## -description

Returns a serialized user credential.

## -parameters

### -param userCredential [out]

Receives a pointer to an instance of [WTS_SERIALIZED_USER_CREDENTIAL](../wtsapi32/ns-wtsapi32-wts_serialized_user_credential.md) containing the serialized credential if the function succeeds. To free the allocated memory, the Remote Desktop Services service calls the *[WTSFreeMemoryEx](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsfreememoryexw)* function and pass **WTSTypeSerializedUserCredential** for the *WTSTypeClass* parameter.
Protocol implementations can transfer the ownership of the credential they obtained using [WTSCloudAuthConvertAssertionToSerializedUserCredential](../wtsapi32/nf-wtsapi32-wtscloudauthconvertassertiontoserializedusercredential.md) (recommended) after which they should not use the credential anymore. Alternatively, protocol implementations can use [WTSCloudAuthDuplicateSerializedUserCredential](../wtsapi32/nf-wtsapi32-wtscloudauthduplicateserializedusercredential.md) to duplicate the serialized credentials obtained from **WTSCloudAuthConvertAssertionToSerializedUserCredential**.

## -returns

If the function succeeds, the function returns **S_OK**. If the function fails, it returns an **HRESULT** value that indicates the error. For a list of common error codes, see **[Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values)**.

## -remarks

If your protocol both returns an **HRESULT** error code in this method and in [IWRdsProtocolConnection::GetUserCredentials](/windows/win32/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getusercredentials), WinLogon will display a logon screen to request credentials. If your protocol returns S_OK, the credentials will be passed to WinLogon to log on the user.

## -see-also
