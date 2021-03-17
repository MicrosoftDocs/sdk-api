---
UID: NC:ntsecpkg.LSA_GET_AUTH_DATA_FOR_USER
title: LSA_GET_AUTH_DATA_FOR_USER (ntsecpkg.h)
description: The GetAuthDataForUser function retrieves authentication information for a user from the Security Accounts Manager (SAM) database and puts it into a format suitable for the ConvertAuthDataToToken function.
helpviewer_keywords: ["GetAuthDataForUser","GetAuthDataForUser callback function [Security]","LSA_GET_AUTH_DATA_FOR_USER","LSA_GET_AUTH_DATA_FOR_USER callback","SecNameAlternateId","SecNameDN","SecNameFlat","SecNameSamCompatible","_ssp_getauthdataforuser","ntsecpkg/GetAuthDataForUser","security.getauthdataforuser"]
old-location: security\getauthdataforuser.htm
tech.root: security
ms.assetid: 1cc02c6b-2628-441d-97ae-ed83a4f6bfd0
ms.date: 12/05/2018
ms.keywords: GetAuthDataForUser, GetAuthDataForUser callback function [Security], LSA_GET_AUTH_DATA_FOR_USER, LSA_GET_AUTH_DATA_FOR_USER callback, SecNameAlternateId, SecNameDN, SecNameFlat, SecNameSamCompatible, _ssp_getauthdataforuser, ntsecpkg/GetAuthDataForUser, security.getauthdataforuser
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_GET_AUTH_DATA_FOR_USER
 - ntsecpkg/LSA_GET_AUTH_DATA_FOR_USER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - GetAuthDataForUser
---

# LSA_GET_AUTH_DATA_FOR_USER callback function


## -description

The <b>GetAuthDataForUser</b> function retrieves authentication information for a user from the Security Accounts Manager (SAM) database and puts it into a format suitable for the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_convert_auth_data_to_token">ConvertAuthDataToToken</a> function.

## -parameters

### -param Name [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that specifies the name of the SAM account.

### -param NameType [in]

A 
<a href="/windows/desktop/api/ntsecpkg/ne-ntsecpkg-secpkg_name_type">SECPKG_NAME_TYPE</a> enumeration value that specifies the type of account name in <i>Name</i>. This parameter can be one of the following values.

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
<i>Name</i> is a flat <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) style account name.

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
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the prefix to use for names specified with the <b>SecNameAlternateId</b> <i>NameType</i>.

### -param UserAuthData [out]

Pointer that receives the address of the retrieved data.

### -param UserAuthDataSize [out]

Pointer to a <b>ULONG</b> that receives the size of the retrieved data.

### -param UserFlatName [out]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that receives the UPN, if applicable.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.

## -remarks

The <b>GetAuthDataForUser</b> function combines the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a>, 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a>, and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_close_sam_user">CloseSamUser</a> functions into one call.

Pointers to these functions are available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_close_sam_user">CloseSamUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data">GetUserAuthData</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
