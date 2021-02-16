---
UID: NC:ntsecpkg.LSA_OPEN_SAM_USER
title: LSA_OPEN_SAM_USER (ntsecpkg.h)
description: Retrieves a handle to a user account in the Security Accounts Manager (SAM) database.
helpviewer_keywords: ["FALSE","LSA_OPEN_SAM_USER","LSA_OPEN_SAM_USER callback","OpenSamUser","OpenSamUser callback function [Security]","SecNameAlternateId","SecNameDN","SecNameFlat","SecNameSamCompatible","TRUE","_ssp_opensamuser","ntsecpkg/OpenSamUser","security.opensamuser"]
old-location: security\opensamuser.htm
tech.root: security
ms.assetid: 1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4
ms.date: 12/05/2018
ms.keywords: FALSE, LSA_OPEN_SAM_USER, LSA_OPEN_SAM_USER callback, OpenSamUser, OpenSamUser callback function [Security], SecNameAlternateId, SecNameDN, SecNameFlat, SecNameSamCompatible, TRUE, _ssp_opensamuser, ntsecpkg/OpenSamUser, security.opensamuser
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
 - LSA_OPEN_SAM_USER
 - ntsecpkg/LSA_OPEN_SAM_USER
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
 - OpenSamUser
---

# LSA_OPEN_SAM_USER callback function


## -description

Retrieves a handle to a user account in the <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) database.

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
<i>Name</i> is in the AltSecId property of the SAM account. This value is used with the <i>Prefix</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="SecNameFlat"></a><a id="secnameflat"></a><a id="SECNAMEFLAT"></a><dl>
<dt><b>SecNameFlat</b></dt>
</dl>
</td>
<td width="60%">
<i>Name</i> is a flat <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN)–style account name.

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
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that specifies the prefix to use with names that use a <i>NameType</i> of SecNameAlternateId.

### -param AllowGuest [in]

Specifies whether to use the Guest account if the SAM account is not found. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
If the user is not found, the <b>OpenSamUser</b> function call fails.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
If the user is not found and the Guest account is enabled, the Guest account is used.

</td>
</tr>
</table>

### -param Reserved [in]

Reserved. Specify zero.

### -param UserHandle [out]

Pointer to a pointer that receives a handle to the user account.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is one of the following  NTSTATUS error codes that indicates the reason for  failure.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>NameType</i> is SecNameAlternateId and <i>Prefix</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The SAM account could not be found.

</td>
</tr>
</table>

## -remarks

To close the handle received by the <i>UserHandle</i> parameter,   call the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_close_sam_user">CloseSamUser</a> function.

The distinguished name of a user identifies the name, domain, and the complete path to the 
<a href="/windows/desktop/AD/active-directory-domain-services">Active Directory</a> object that represents the user.

A pointer to the <b>OpenSamUser</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_close_sam_user">CloseSamUser</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
