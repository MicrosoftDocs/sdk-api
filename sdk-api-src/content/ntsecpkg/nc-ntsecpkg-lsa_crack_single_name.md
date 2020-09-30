---
UID: NC:ntsecpkg.LSA_CRACK_SINGLE_NAME
title: LSA_CRACK_SINGLE_NAME (ntsecpkg.h)
description: The CrackSingleName function converts a name from one format to another.
helpviewer_keywords: ["CrackSingleName","CrackSingleName callback function [Security]","DS_CANONICAL_NAME","DS_CANONICAL_NAME_EX","DS_DISPLAY_NAME","DS_FQDN_1779_NAME","DS_NT4_ACCOUNT_NAME","DS_SERVICE_PRINCIPAL_NAME","DS_SID_OR_SID_HISTORY_NAME","DS_UNIQUE_ID_NAME","DS_UNKNOWN_NAME","DS_USER_PRINCIPAL_NAME","LSA_CRACK_SINGLE_NAME","LSA_CRACK_SINGLE_NAME callback","_ssp_cracksinglename","ntsecpkg/CrackSingleName","security.cracksinglename"]
old-location: security\cracksinglename.htm
tech.root: security
ms.assetid: de42ca97-4ce2-4bfb-abd1-7409cc5c09a8
ms.date: 12/05/2018
ms.keywords: CrackSingleName, CrackSingleName callback function [Security], DS_CANONICAL_NAME, DS_CANONICAL_NAME_EX, DS_DISPLAY_NAME, DS_FQDN_1779_NAME, DS_NT4_ACCOUNT_NAME, DS_SERVICE_PRINCIPAL_NAME, DS_SID_OR_SID_HISTORY_NAME, DS_UNIQUE_ID_NAME, DS_UNKNOWN_NAME, DS_USER_PRINCIPAL_NAME, LSA_CRACK_SINGLE_NAME, LSA_CRACK_SINGLE_NAME callback, _ssp_cracksinglename, ntsecpkg/CrackSingleName, security.cracksinglename
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
 - LSA_CRACK_SINGLE_NAME
 - ntsecpkg/LSA_CRACK_SINGLE_NAME
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
 - CrackSingleName
---

# LSA_CRACK_SINGLE_NAME callback function


## -description

The <b>CrackSingleName</b> function converts a name from one format to another.

## -parameters

### -param FormatOffered [in]

The format of the input name. The following table contains the valid values for this parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DS_CANONICAL_NAME"></a><a id="ds_canonical_name"></a><dl>
<dt><b>DS_CANONICAL_NAME</b></dt>
</dl>
</td>
<td width="60%">
Complete canonical name (for example, example.microsoft.com/software/someone). The domain-only version includes a trailing forward slash (/).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_CANONICAL_NAME_EX"></a><a id="ds_canonical_name_ex"></a><dl>
<dt><b>DS_CANONICAL_NAME_EX</b></dt>
</dl>
</td>
<td width="60%">
Same as DS_CANONICAL_NAME except that the rightmost forward slash (/) is replaced with a newline character (\n), even in a domain-only case (for example, example.microsoft.com/software\nsomeone).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_DISPLAY_NAME"></a><a id="ds_display_name"></a><dl>
<dt><b>DS_DISPLAY_NAME</b></dt>
</dl>
</td>
<td width="60%">
A "friendly" display name. The display name is not necessarily the defining <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_FQDN_1779_NAME"></a><a id="ds_fqdn_1779_name"></a><dl>
<dt><b>DS_FQDN_1779_NAME</b></dt>
</dl>
</td>
<td width="60%">
Fully qualified distinguished name (for example, CN=NameOfPerson,OU=Users,DC=Example,DC=Fabrikam,DC=Com).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_NT4_ACCOUNT_NAME"></a><a id="ds_nt4_account_name"></a><dl>
<dt><b>DS_NT4_ACCOUNT_NAME</b></dt>
</dl>
</td>
<td width="60%">
Windows account name (for example, Example\Name). The domain-only version includes trailing backslashes (\\).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_SERVICE_PRINCIPAL_NAME"></a><a id="ds_service_principal_name"></a><dl>
<dt><b>DS_SERVICE_PRINCIPAL_NAME</b></dt>
</dl>
</td>
<td width="60%">
Generalized <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (for example, www/www.microsoft.com@microsoft.com).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_SID_OR_SID_HISTORY_NAME"></a><a id="ds_sid_or_sid_history_name"></a><dl>
<dt><b>DS_SID_OR_SID_HISTORY_NAME</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) for the object. This can be either the current SID or a SID from the object's SID history. The SID string can use either the standard string representation of a SID, or one of the string constants defined in Sddl.h. For information about converting a binary SID into a SID string, see <a href="/windows/desktop/SecAuthZ/sid-strings">SID Strings</a>. This value is not valid for the <i>formatDesired</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DS_UNIQUE_ID_NAME"></a><a id="ds_unique_id_name"></a><dl>
<dt><b>DS_UNIQUE_ID_NAME</b></dt>
</dl>
</td>
<td width="60%">
GUID string that the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-iidfromstring">IIDFromString</a> function returns (for example, {4fa050f0-f561-11cf-bdd9-00aa003a77b6}).

</td>
</tr>
<tr>
<td width="40%"><a id="DS_UNKNOWN_NAME"></a><a id="ds_unknown_name"></a><dl>
<dt><b>DS_UNKNOWN_NAME</b></dt>
</dl>
</td>
<td width="60%">
Unknown name type.

</td>
</tr>
<tr>
<td width="40%"><a id="DS_USER_PRINCIPAL_NAME"></a><a id="ds_user_principal_name"></a><dl>
<dt><b>DS_USER_PRINCIPAL_NAME</b></dt>
</dl>
</td>
<td width="60%">
User principal name (for example, someone@example.microsoft.com).

</td>
</tr>
</table>

### -param PerformAtGC [in]

Specifies whether to perform the translation at a global catalog server.

### -param NameInput [in]

A pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the name to convert.

### -param Prefix [in, optional]

A pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that specifies a prefix for the name.

### -param RequestedFormat [in]

The requested format of the cracked name. For a list of valid values, see the <i>FormatOffered</i> parameter.

### -param CrackedName [out]

A pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that receives the reformatted name.

### -param DnsDomainName [out]

A pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that receives the name of the domain that owns the name specified by the <i>NameInput</i> parameter.

### -param SubStatus [out]

A pointer to a variable that receives additional information about the return value of the function call.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns STATUS_UNSUCCESSFUL. For more information, see the value returned in the <i>SubStatus</i> parameter.

## -remarks

A pointer to the <b>CrackSingleName</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>