---
UID: NC:ntsecpkg.CredWriteFn
title: CredWriteFn
author: windows-driver-content
description: Writes the specified credential to the Credential Manager.
old-location: security\crediwrite.htm
old-project: SecAuthN
ms.assetid: 19c7fe4d-9c7b-4547-baab-443483deb013
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CREDP_FLAGS_CLEAR_PASSWORD, CREDP_FLAGS_DONT_CACHE_TI, CREDP_FLAGS_IN_PROCESS, CREDP_FLAGS_TRUSTED_CALLER, CREDP_FLAGS_USER_ENCRYPTED_PASSWORD, CREDP_FLAGS_USE_MIDL_HEAP, CredWriteFn, CrediWrite, CrediWrite function [Security], ntsecpkg/CrediWrite, security.crediwrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CrediWrite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CredWriteFn callback function


## -description


Writes the specified credential to the <a href="https://msdn.microsoft.com/a1105754-a57f-4a0d-9797-bec22b99900c">Credential Manager</a>.


## -parameters




### -param LogonId [in]

The logon ID for which to read credentials.


### -param CredFlags [in]

Flags that determine the behavior of this function. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_IN_PROCESS"></a><a id="credp_flags_in_process"></a><dl>
<dt><b>CREDP_FLAGS_IN_PROCESS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The caller is in-process.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_USE_MIDL_HEAP"></a><a id="credp_flags_use_midl_heap"></a><dl>
<dt><b>CREDP_FLAGS_USE_MIDL_HEAP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The caller should use the <a href="https://msdn.microsoft.com/3def405c-da05-4cce-9dc4-499864a0de6e">midl_user_allocate</a> function to allocate the <i>Credential</i> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_DONT_CACHE_TI"></a><a id="credp_flags_dont_cache_ti"></a><dl>
<dt><b>CREDP_FLAGS_DONT_CACHE_TI</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Do not cache target information.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_CLEAR_PASSWORD"></a><a id="credp_flags_clear_password"></a><dl>
<dt><b>CREDP_FLAGS_CLEAR_PASSWORD</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The credential data is passed as clear text.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_USER_ENCRYPTED_PASSWORD"></a><a id="credp_flags_user_encrypted_password"></a><dl>
<dt><b>CREDP_FLAGS_USER_ENCRYPTED_PASSWORD</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The credential data is encrypted by using the <a href="https://msdn.microsoft.com/b124a7fe-c62c-42f7-9d2b-cbf74d17186a">RtlEncryptMemory</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_TRUSTED_CALLER"></a><a id="credp_flags_trusted_caller"></a><dl>
<dt><b>CREDP_FLAGS_TRUSTED_CALLER</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The caller is a trusted process.

</td>
</tr>
</table>
 


### -param Credential [in]

A pointer to an <a href="https://msdn.microsoft.com/b350ef3d-5ed5-4355-ae3a-f03fafff2f52">ENCRYPTED_CREDENTIALW</a> structure that represents the credentials to write.


### -param Flags [in]

Reserved. This parameter must be set to zero.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.




## -remarks



A pointer to the <b>CrediWrite</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

