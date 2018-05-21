---
UID: NC:ntsecpkg.SpQueryCredentialsAttributesFn
title: SpQueryCredentialsAttributesFn
author: windows-driver-content
description: Retrieves the attributes for a credential.
old-location: security\spquerycredentialsattributes.htm
old-project: SecAuthN
ms.assetid: e9174a42-3ccd-4c9a-bf80-fba062df4459
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SECPKG_ATTR_CIPHER_STRENGTHS, SECPKG_ATTR_SUPPORTED_ALGS, SECPKG_ATTR_SUPPORTED_PROTOCOLS, SECPKG_CRED_ATTR_NAMES, SpQueryCredentialsAttributes, SpQueryCredentialsAttributes function [Security], SpQueryCredentialsAttributesFn, _ssp_spquerycredentialsattributes, ntsecpkg/SpQueryCredentialsAttributes, security.spquerycredentialsattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
-	SpQueryCredentialsAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpQueryCredentialsAttributesFn callback function


## -description


The <b>SpQueryCredentialsAttributes</b> function retrieves the attributes for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credential</a>.

The <b>SpQueryCredentialsAttributes</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param CredentialHandle [in]

A handle to the credential to query.


### -param CredentialAttribute [in]

<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Attribute</a> to query. The following table lists the valid values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_ATTR_NAMES"></a><a id="secpkg_cred_attr_names"></a><dl>
<dt><b>SECPKG_CRED_ATTR_NAMES</b></dt>
</dl>
</td>
<td width="60%">
The name of the principal associated with the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUPPORTED_ALGS"></a><a id="secpkg_attr_supported_algs"></a><dl>
<dt><b>SECPKG_ATTR_SUPPORTED_ALGS</b></dt>
</dl>
</td>
<td width="60%">
The algorithms supported with a particular credential.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CIPHER_STRENGTHS"></a><a id="secpkg_attr_cipher_strengths"></a><dl>
<dt><b>SECPKG_ATTR_CIPHER_STRENGTHS</b></dt>
</dl>
</td>
<td width="60%">
The minimum and maximum cipher strength used with a credential.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUPPORTED_PROTOCOLS"></a><a id="secpkg_attr_supported_protocols"></a><dl>
<dt><b>SECPKG_ATTR_SUPPORTED_PROTOCOLS</b></dt>
</dl>
</td>
<td width="60%">
The protocols supported with a particular credential.

</td>
</tr>
</table>
 


### -param Buffer [out]

Pointer to a buffer that receives the requested attributes. Allocate memory for this buffer using the 
<a href="https://msdn.microsoft.com/2a7dfc11-a8ab-4677-ad5c-b2f4b5998efe">AllocateClientBuffer</a> function, so that caller can free it by calling the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists common reasons for failure and the error codes that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The credential handle is not valid.

</td>
</tr>
</table>
 




## -remarks



SSP/APs must implement the <b>SpQueryCredentialsAttributes</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpQueryCredentialsAttributes</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

