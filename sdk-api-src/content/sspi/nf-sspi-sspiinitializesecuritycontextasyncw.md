---
UID: NF:sspi.SspiInitializeSecurityContextAsyncW
title: SspiInitializeSecurityContextAsyncW function
ms.date: 11/4/2019
targetos: Windows
description: Initializes an async security context. (Unicode)
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
 - SspiInitializeSecurityContextAsyncW
f1_keywords:
 - SspiInitializeSecurityContextAsyncW
 - sspi/SspiInitializeSecurityContextAsyncW
dev_langs:
 - c++
---

## -description

The **SspiInitializeSecurityContextAsyncW** function initiates the client side, outbound <a href="/windows/desktop/SecGloss/s-gly">security context</a> from a credential handle. The function is used to build a security context between the client application and a remote peer. **SspiInitializeSecurityContextAsyncW** returns a token that the client must pass to the remote peer, which the peer in turn submits to the local security implementation through the 
[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md) call.

> [!NOTE]
> This function serves as the asynchronous counterpart to the [InitializeSecurityContext function](/windows/win32/secauthn/initializesecuritycontext--general).

## -parameters

### -param AsyncContext

The async call context.

### -param phCredential

A handle to the credentials returned by 
[AcquireCredentialsHandle](nf-sspi-sspiacquirecredentialshandleasynca.md). This handle is used to build the <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

### -param phContext

A pointer to an existing [CtxtHandle](/windows/desktop/SecAuthN/sspi-handles) structure.

### -param pszTargetName

A pointer to a null-terminated string that indicates the target of the context. The string contents are [*security package*](/windows/win32/secgloss/s-gly) specific, as described in the following table. This list is not exhaustive. Additional system SSPs and third party SSPs can be added to a system.

| SSP in use | Meaning |
|---|---|
| **Digest** | Null-terminated string that uniquely identifies the URI of the requested resource. The string must be composed of characters that are allowed in a URI and must be representable by the US ASCII code set. Percent encoding can be used to represent characters outside the US ASCII code set. |
| **Kerberos or Negotiate** | Service principal name (SPN) or the [security context](/windows/win32/secgloss/s-gly) of the destination server. |
| **NTLM** | Service principal name (SPN) or the [security context](/windows/win32/secgloss/s-gly) of the destination server. |
| **Schannel/SSL** | Null-terminated string that uniquely identifies the target server. Schannel uses this value to verify the server certificate. Schannel also uses this value to locate the session in the session cache when reestablishing a connection. The cached session is used only if all of the following conditions are met: <ul><li> The target name is the same.</li><li>The cache entry has not expired.<li>The application process that calls the function is the same.<li>The logon session is the same.<li>The credential handle is the same.</li></li></li></li></ul> |

### -param fContextReq

Bit flags that indicate requests for the context.

See [InitializeSecurityContext: fContextReq](/windows/win32/secauthn/initializesecuritycontext--general#parameters) for a list of flag values and their meanings.

### -param Reserved1

This parameter is reserved and must be set to zero.

### -param TargetDataRep

The data representation, such as byte ordering, on the target. This parameter can be either SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.

### -param pInput

A pointer to a [SecBufferDesc](./ns-sspi-secbufferdesc.md) structure that contains pointers to the buffers supplied as input to the package.

### -param Reserved2

This parameter is reserved and must be set to zero.

### -param phNewContext

A pointer to a [CtxtHandle](/windows/win32/secauthn/sspi-handles) structure.

### -param pOutput

A pointer to a [SecBufferDesc](./ns-sspi-secbufferdesc.md) structure that contains pointers to the SecBuffer structure that receives the output data.

### -param pfContextAttr

A pointer to a variable to receive a set of bit flags that indicate the attributes of the established context. For a description of the various attributes, see [Context Requirements](/windows/win32/secauthn/context-requirements).

### -param ptsExpiry

*Optional*. A pointer to a [TimeStamp](/windows/win32/secauthn/timestamp) structure that receives the expiration time of the context.

## -returns

Returns **SEC_E_OK** if the async request to establish a security context was successfully queued for execution, otherwise, returns the error generated attempting to queue it. To retrieve the status of the operation, use [SspiGetAsyncCallStatus](nf-sspi-sspigetasynccallstatus.md).

If the security context received from the server was accepted, SspiGetAsyncCallStatus returns **SEC_E_OK** or one of the SSPI codes in the table below. Otherwise, it may return **SEC_I_ASYNC_CALL_PENDING** if the call is still in progress, or any of the following fatal error codes in the second table below.

|<div>Return code</div>|<div>Description</div>|
|---|---|
|**SEC_I_COMPLETE_AND_CONTINUE**<br>0x00090314L| The client must call [CompleteAuthToken](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) and pass the output token to the server. The client then waits for a returned token and passes it, in another call, to SspiInitializeSecurityContextAsyncA. |
|**SEC_I_COMPLETE_NEEDED**<br>0x00090313L |  The client must finish building the message from the server before calling [CompleteAuthToken](/windows/desktop/api/sspi/nf-sspi-completeauthtoken).|
|**SEC_I_CONTINUE_NEEDED**<br>0x00090312L| The client must send the output token to the server and wait for a return token. The returned token is then passed in another call to SspiInitializeSecurityContextAsyncA. The output token can be empty. |
| **SEC_I_INCOMPLETE_CREDENTIALS** | Use with Schannel. The server has requested client authentication, and the supplied credentials either do not include a certificate or the certificate was not issued by a certification authority that is trusted by the server. |
|**SEC_E_INCOMPLETE_MESSAGE**<br>0x80090318L |  Data for the whole message was not read from the wire. When this value is returned, the pInput buffer contains a SecBuffer structure with a BufferType member of SECBUFFER_MISSING. The cbBuffer member of SecBuffer contains a value that indicates the number of additional bytes that the function must read from the client before this function succeeds. While this number is not always accurate, using it can help improve performance by avoiding multiple calls to this function.|
|**SEC_E_OK**<br>0x00000000L| The security context received from the client was accepted. If the function generated an output token, the token must be sent to the server.|

### Fatal error codes

|<div>Return code</div>|<div>Description</div>|
|---|---|
|**SEC_E_INSUFFICIENT_MEMORY**<br>0x80090300L|There is not enough memory available to complete the requested action.|
|**SEC_E_INTERNAL_ERROR**<br>0x80090304L| An error occurred that did not map to an SSPI error code.|
|**SEC_E_INVALID_HANDLE**<br>0x80100003L| The handle passed to the function is not valid.|
|**SEC_E_INVALID_TOKEN**<br>0x80090308L| The error is due to a malformed input token, such as a token corrupted in transit, a token of incorrect size, or a token passed into the wrong security package. Passing a token to the wrong package can happen if the client and server did not negotiate the proper security package.|
|**SEC_E_LOGON_DENIED**<br>0x8009030CL|The logon failed.|
|**SEC_E_NO_AUTHENTICATING_AUTHORITY**<br>0x80090311L |  No authority could be contacted for authentication. The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.|
|**SEC_E_NO_CREDENTIALS**<br>0x8009030EL| No credentials are available in the security package.|
| **SEC_E_TARGET_UNKNOWN** | The target was not recognized.|
|**SEC_E_UNSUPPORTED_FUNCTION**<br>0x80090302L| A context attribute flag that is not valid (ISC_REQ_DELEGATE or ISC_REQ_PROMPT_FOR_CREDS) was specified in the fContextReq parameter.|
| **SEC_E_WRONG_PRINCIPAL** | The principal that received the authentication request is not the same as the one passed into the pszTargetName parameter. This indicates a failure in mutual authentication. |

## -remarks

See [InitializeSecurityContext](/windows/win32/secauthn/initializesecuritycontext--general#remarks) for complete remarks.

## -see-also

[SspiAcceptSecurityContextAsync](nf-sspi-sspiacceptsecuritycontextasync.md)

[SspiAcquireCredentialsHandleAsync](nf-sspi-sspiacquirecredentialshandleasynca.md)
