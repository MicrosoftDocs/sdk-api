---
UID: NF:sspi.SspiAcquireCredentialsHandleAsyncA
title: SspiAcquireCredentialsHandleAsyncA function
ms.date: 11/4/2019
targetos: Windows
description: Asynchronously acquires a handle to preexisting credentials of a security principal. (ANSI)
tech.root: security
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1607 [kernel-mode drivers only]
req.target-min-winversvr: Windows Server 2016 [kernel-mode drivers only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - sspi.h
api_name:
 - SspiAcquireCredentialsHandleAsyncA
f1_keywords:
 - SspiAcquireCredentialsHandleAsyncA
 - sspi/SspiAcquireCredentialsHandleAsyncA
dev_langs:
 - c++
---

# SspiAcquireCredentialsHandleAsyncA function


## -description

The **SspiAcquireCredentialsHandleAsyncA** function asynchronously acquires a handle to preexisting [credentials](/windows/desktop/SecGloss/c-gly) of a [security principal](/windows/desktop/SecGloss/s-gly). 

This handle is required by the 
[SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md) and 
[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md) functions. These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.
			
> [!NOTE]
> This function serves as the asynchronous counterpart to [AcquireCredentialsHandle](/windows/win32/secauthn/acquirecredentialshandle--general).

## -parameters

### -param AsyncContext

The async call context.

### -param pszPrincipal

A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference asynchronously.

### -param pszPackage

A pointer to a null-terminated string that specifies the name of the [security package](/windows/desktop/SecGloss/s-gly) with which these credentials will be used. 

See [AcquireCredentialsHandleA: pszPackage](/windows/win32/secauthn/acquirecredentialshandle--general#parameters)

### -param fCredentialUse

A flag that indicates how these credentials will be used. This parameter can be one of the following values:

|<div>Value</div>|<div>Meaning</div>|
|---|---|
| **SECPKG_CRED_INBOUND** | Validate an incoming server credential. Inbound credentials might be validated by using an authenticating authority when [SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md) or [SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md) is called. If such an authority is not available, the function will fail and return **SEC_E_NO_AUTHENTICATING_AUTHORITY**. Validation is package specific.|
| **SECPKG_CRED_OUTBOUND** | Allow a local client credential to prepare an outgoing token.|

### -param pvLogonId

A pointer to a [locally unique identifier](/windows/desktop/SecGloss/l-gly) (LUID) that identifies the user. This parameter is provided for file-system processes such as network redirectors. This parameter can be **NULL**.

### -param pAuthData

A pointer to a [CREDSSP_CRED](/windows/desktop/api/credssp/ns-credssp-credssp_cred) structure that specifies authentication data for both Schannel and Negotiate packages.

### -param pGetKeyFn

Pointer to the GetKey() function.

### -param pvGetKeyArgument

Pass to GetKey().

### -param phCredential

A pointer to the [CredHandle](/windows/desktop/SecAuthN/sspi-handles) structure that will receive the credential handle.

### -param ptsExpiry

*optional* A pointer to a [TimeStamp](/windows/desktop/SecAuthN/timestamp) structure that receives the time at which the returned credentials expire. The structure value received depends on the security package, which must specify the value in local time.

## -returns

Returns **SEC_E_OK** if the async request to acquire a credential handle was successfully queued for execution. Otherwise, it returns the error generated attempting to queue it. To retrieve the status of the operation, use [SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md).

If the handle was acquired, SspiGetAsyncCallStatus returns **SEC_E_OK**. Otherwise, it may return *SEC_I_ASYNC_CALL_PENDING* if the call is still in progress, or any of the following fatal error codes in the table below.

|<div>Return code</div>|<div>Description</div>|
|---|---|
| **SEC_E_INSUFFICIENT_MEMORY** | There is insufficient memory available to complete the requested action. |
| **SEC_E_INTERNAL_ERROR** | An error occurred that did not map to an SSPI error code. |
| **SEC_E_NO_CREDENTIALS** | No credentials are available in the [security package](/windows/desktop/SecGloss/s-gly) |
| **SEC_E_NOT_OWNER** | The caller of the function does not have the necessary credentials. |
| **SEC_E_SECPKG_NOT_FOUND** | The requested security package does not exist.|
| **SEC_E_UNKNOWN_CREDENTIALS** | The credentials supplied to the package were not recognized. |

## -remarks

The **SspiAcquireCredentialsHandleAsyncA** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [security package](/windows/desktop/SecGloss/s-gly). The function can return the handle to either preexisting credentials or newly created credentials and return it. This handle can be used in subsequent calls to the 
[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md) and 
[SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md) functions.

In general, **SspiAcquireCredentialsHandleAsyncA** does not provide  the credentials of other users logged on to the same computer. However, a caller with SE_TCB_NAME  [privilege](/windows/desktop/SecGloss/p-gly) can obtain the [credentials](/windows/desktop/SecGloss/c-gly) of an existing logon session by specifying the [logon identifier](/windows/desktop/SecGloss/l-gly) (LUID) of that session. Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.

A package might call the function in *pGetKeyFn* provided by the RPC run-time transport. If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.

For kernel mode callers, the following differences must be noted:

- The two string parameters must be [Unicode](/windows/desktop/SecGloss/u-gly) strings.
- The buffer values must be allocated in process virtual memory, not from the pool.

When you have finished using the returned credentials, free the memory used by the credentials by calling the 
[SspiFreeCredentialsHandleAsync](nf-sspi-sspifreecredentialshandleasync.md) function.

## -see-also

[AcquireCredentialsHandle](/windows/win32/secauthn/acquirecredentialshandle--general)

[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md)

[SspiFreeCredentialsHandleAsync](nf-sspi-sspifreecredentialshandleasync.md)

[SspiInitializeSecurityContextAsync](nf-sspi-sspiinitializesecuritycontextasynca.md)

[SSPI Functions](/windows/desktop/SecAuthN/authentication-functions)

