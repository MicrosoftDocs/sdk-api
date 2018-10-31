---
UID: NF:sspi.SetCredentialsAttributesW
title: SetCredentialsAttributesW function
author: windows-sdk-content
description: Sets the attributes of a credential, such as the name associated with the credential.
old-location: security\setcredentialsattributes.htm
tech.root: secauthn
ms.assetid: 419fb4f0-3dd1-4473-aeb2-8024355e0c1c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: QueryCredentialsAttributesA, QueryCredentialsAttributesW, SetCredentialsAttributes, SetCredentialsAttributes function [Security], SetCredentialsAttributesA, SetCredentialsAttributesW, security.setcredentialsattributes, sspi/QueryCredentialsAttributesA, sspi/QueryCredentialsAttributesW, sspi/SetCredentialsAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryCredentialsAttributesW (Unicode) and QueryCredentialsAttributesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - SetCredentialsAttributes
 - QueryCredentialsAttributesA
 - QueryCredentialsAttributesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCredentialsAttributesW function


## -description


Sets the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credential</a>, such as the name associated with the credential. The information is valid for any <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> created with the specified credential.


## -parameters




### -param phCredential [in]

A handle of the credentials to be set.


### -param ulAttribute [in]

Specifies the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to set. This parameter can be any of the following attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_NAMES</dt>
</dl>
</td>
<td width="60%">
Sets the name of a credential in a <i>pBuffer</i> parameter of type <a href="https://msdn.microsoft.com/38123a10-72a4-46eb-974b-3c01142dfc74">SecPkgCredentials_Names</a>.

This attribute is not supported by Schannel in WOW64 mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_CRED_ATTR_KDC_PROXY_SETTINGS</dt>
</dl>
</td>
<td width="60%">
Sets the Kerberos proxy setting in a  <i>pBuffer</i> parameter of type <a href="https://msdn.microsoft.com/42BC75B8-6392-4FD4-95BC-266B3AFDDC62">SecPkgCredentials_KdcProxySettings</a>.

This attribute is only supported by Kerberos.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_SUPPORTED_ALGS</dt>
</dl>
</td>
<td width="60%">
Sets the supported algorithms in a  <i>pBuffer</i> parameter of type <a href="https://msdn.microsoft.com/3beb83bb-759c-4025-93ce-d9827890c60e">SecPkgCred_SupportedAlgs</a>. All supported algorithms are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

This attribute is supported only by Schannel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_CIPHER_STRENGTHS</dt>
</dl>
</td>
<td width="60%">
Sets the cipher strengths in a <i>pBuffer</i> parameter of type <a href="https://msdn.microsoft.com/e4d3be07-0f37-470a-a760-f704c18c6826">SecPkgCred_CipherStrengths</a>.

This attribute is supported only by Schannel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SECPKG_ATTR_SUPPORTED_PROTOCOLS</dt>
</dl>
</td>
<td width="60%">
Sets the supported algorithms in a <i>pBuffer</i> parameter of type <a href="https://msdn.microsoft.com/712f93f2-11b9-4533-bb5d-507b25ede378">SecPkgCred_SupportedProtocols</a>. All supported protocols are included, regardless of whether they are supported by the provided certificate or enabled on the local computer.

This attribute is supported only by Schannel.

</td>
</tr>
</table>
 


### -param pBuffer [in]

A pointer to a buffer that contains the new attribute value. The type of structure returned depends on the value of <i>ulAttribute</i>.


### -param cbBuffer

The size, in bytes, of the <i>pBuffer</i> buffer.


## -returns



If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value may be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The specified <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> is not supported by Schannel. This return value will only be returned when the Schannel SSP is being used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the request.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/8398e029-473e-488f-a861-c7ceae07e678">SCHANNEL_CRED</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/e4d3be07-0f37-470a-a760-f704c18c6826">SecPkgCred_CipherStrengths</a>



<a href="https://msdn.microsoft.com/3beb83bb-759c-4025-93ce-d9827890c60e">SecPkgCred_SupportedAlgs</a>



<a href="https://msdn.microsoft.com/712f93f2-11b9-4533-bb5d-507b25ede378">SecPkgCred_SupportedProtocols</a>



<a href="https://msdn.microsoft.com/38123a10-72a4-46eb-974b-3c01142dfc74">SecPkgCredentials_Names</a>
 

 

