---
UID: NC:ntsecpkg.LSA_GET_AUTH_DATA_FOR_USER
title: LSA_GET_AUTH_DATA_FOR_USER
author: windows-driver-content
description: The GetAuthDataForUser function retrieves authentication information for a user from the Security Accounts Manager (SAM) database and puts it into a format suitable for the ConvertAuthDataToToken function.
old-location: security\getauthdataforuser.htm
old-project: SecAuthN
ms.assetid: 1cc02c6b-2628-441d-97ae-ed83a4f6bfd0
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: GetAuthDataForUser, GetAuthDataForUser function [Security], LSA_GET_AUTH_DATA_FOR_USER, SecNameAlternateId, SecNameDN, SecNameFlat, SecNameSamCompatible, _ssp_getauthdataforuser, ntsecpkg/GetAuthDataForUser, security.getauthdataforuser
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
-	GetAuthDataForUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# LSA_GET_AUTH_DATA_FOR_USER callback


## -description


The <b>GetAuthDataForUser</b> function retrieves authentication information for a user from the Security Accounts Manager (SAM) database and puts it into a format suitable for the 
<a href="https://msdn.microsoft.com/99dfd3b3-40e0-44b2-8752-39b7b394ac0e">ConvertAuthDataToToken</a> function.


## -parameters




### -param Name [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that specifies the name of the SAM account.


### -param NameType [in]

A 
<a href="https://msdn.microsoft.com/6a534bfa-83ec-408d-ad21-e230a7adc61e">SECPKG_NAME_TYPE</a> enumeration value that specifies the type of account name in <i>Name</i>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SecNameSamCompatible"></a><a id="secnamesamcompatible"></a><a id="SECNAMESAMCOMPATIBLE"></a><dl>
<dt><b>SecNameSamCompatible</b></dt>
</dl>
</td>
<td width="60%">
<i>Name</i> is compatible with the SAM. An example of a name in SAM-compatible format is "ExampleDomain\Username".

</td>
</tr>
<tr>
<td width="40%"><a id="SecNameAlternateId"></a><a id="secnamealternateid"></a><a id="SECNAMEALTERNATEID"></a><dl>
<dt><b>SecNameAlternateId</b></dt>
</dl>
</td>
<td width="60%">
<i>Name</i> is in the AltSecId property of the SAM account. You must specify a value for the <i>Prefix</i> parameter when using this value.

</td>
</tr>
<tr>
<td width="40%"><a id="SecNameFlat"></a><a id="secnameflat"></a><a id="SECNAMEFLAT"></a><dl>
<dt><b>SecNameFlat</b></dt>
</dl>
</td>
<td width="60%">
<i>Name</i> is a flat <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) style account name.

</td>
</tr>
<tr>
<td width="40%"><a id="SecNameDN"></a><a id="secnamedn"></a><a id="SECNAMEDN"></a><dl>
<dt><b>SecNameDN</b></dt>
</dl>
</td>
<td width="60%">
<i>Name</i> is the distinguished name of the object. For more information, see  Remarks.

</td>
</tr>
</table>
 


### -param Prefix [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that contains the prefix to use for names specified with the <b>SecNameAlternateId</b> <i>NameType</i>.


### -param *UserAuthData [out]

Pointer that receives the address of the retrieved data.


### -param UserAuthDataSize [out]

Pointer to a <b>ULONG</b> that receives the size of the retrieved data.


### -param UserFlatName [out]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that receives the UPN, if applicable.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.




## -remarks



The <b>GetAuthDataForUser</b> function combines the 
<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a>, 
<a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a>, and 
<a href="https://msdn.microsoft.com/1e56e38e-ba8f-4781-80f1-e60bd33250e4">CloseSamUser</a> functions into one call.

Pointers to these functions are available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1e56e38e-ba8f-4781-80f1-e60bd33250e4">CloseSamUser</a>



<a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

