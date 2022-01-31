---
UID: NE:ntdsapi.__unnamed_enum_0
title: DS_NAME_FORMAT (ntdsapi.h)
description: The DS_NAME_FORMAT enumeration provides formats to use for input and output names for the DsCrackNames function.
helpviewer_keywords: ["DS_CANONICAL_NAME","DS_CANONICAL_NAME_EX","DS_DISPLAY_NAME","DS_DNS_DOMAIN_NAME","DS_FQDN_1779_NAME","DS_NAME_FORMAT","DS_NAME_FORMAT enumeration [Active Directory]","DS_NT4_ACCOUNT_NAME","DS_SERVICE_PRINCIPAL_NAME","DS_SID_OR_SID_HISTORY_NAME","DS_UNIQUE_ID_NAME","DS_UNKNOWN_NAME","DS_USER_PRINCIPAL_NAME","_glines_ds_name_format","ad.ds__name__format","ad.ds_name_format","ntdsapi/DS_CANONICAL_NAME","ntdsapi/DS_CANONICAL_NAME_EX","ntdsapi/DS_DISPLAY_NAME","ntdsapi/DS_DNS_DOMAIN_NAME","ntdsapi/DS_FQDN_1779_NAME","ntdsapi/DS_NAME_FORMAT","ntdsapi/DS_NT4_ACCOUNT_NAME","ntdsapi/DS_SERVICE_PRINCIPAL_NAME","ntdsapi/DS_SID_OR_SID_HISTORY_NAME","ntdsapi/DS_UNIQUE_ID_NAME","ntdsapi/DS_UNKNOWN_NAME","ntdsapi/DS_USER_PRINCIPAL_NAME"]
old-location: ad\ds_name_format.htm
tech.root: ad
ms.assetid: 7a99e531-5a38-4352-8921-7b5a765ffd03
ms.date: 12/05/2018
ms.keywords: DS_CANONICAL_NAME, DS_CANONICAL_NAME_EX, DS_DISPLAY_NAME, DS_DNS_DOMAIN_NAME, DS_FQDN_1779_NAME, DS_NAME_FORMAT, DS_NAME_FORMAT enumeration [Active Directory], DS_NT4_ACCOUNT_NAME, DS_SERVICE_PRINCIPAL_NAME, DS_SID_OR_SID_HISTORY_NAME, DS_UNIQUE_ID_NAME, DS_UNKNOWN_NAME, DS_USER_PRINCIPAL_NAME, _glines_ds_name_format, ad.ds__name__format, ad.ds_name_format, ntdsapi/DS_CANONICAL_NAME, ntdsapi/DS_CANONICAL_NAME_EX, ntdsapi/DS_DISPLAY_NAME, ntdsapi/DS_DNS_DOMAIN_NAME, ntdsapi/DS_FQDN_1779_NAME, ntdsapi/DS_NAME_FORMAT, ntdsapi/DS_NT4_ACCOUNT_NAME, ntdsapi/DS_SERVICE_PRINCIPAL_NAME, ntdsapi/DS_SID_OR_SID_HISTORY_NAME, ntdsapi/DS_UNIQUE_ID_NAME, ntdsapi/DS_UNKNOWN_NAME, ntdsapi/DS_USER_PRINCIPAL_NAME
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DS_NAME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_NAME_FORMAT
 - ntdsapi/DS_NAME_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_NAME_FORMAT
---

# DS_NAME_FORMAT enumeration


## -description

The <b>DS_NAME_FORMAT</b> enumeration provides formats to use for input and output names for the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function.

## -enum-fields

### -field DS_UNKNOWN_NAME:0

Indicates the name is using an unknown name type. This format can impact performance because it forces the server to attempt to match all possible
    formats. Only use this value if the input format is unknown.

### -field DS_FQDN_1779_NAME:1

Indicates that the fully qualified distinguished name is used. For example:

CN=someone,OU=Users,DC=Engineering,DC=Fabrikam,DC=Com

### -field DS_NT4_ACCOUNT_NAME:2

Indicates a Windows NT 4.0 account name. For example:

Engineering\someone

The domain-only version includes two trailing backslashes (\\).

### -field DS_DISPLAY_NAME:3

Indicates a user-friendly display name, for example, Jeff Smith. The display name is not necessarily the same as relative distinguished name (RDN).

### -field DS_UNIQUE_ID_NAME:6

Indicates a GUID string that the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iidfromstring">IIDFromString</a> function returns. For example:

{4fa050f0-f561-11cf-bdd9-00aa003a77b6}

### -field DS_CANONICAL_NAME:7

Indicates a complete canonical name. For example:

engineering.fabrikam.com/software/someone

The domain-only version includes a trailing forward slash (/).

### -field DS_USER_PRINCIPAL_NAME:8

Indicates that it is using the user principal name (UPN). For example:

someone@engineering.fabrikam.com

### -field DS_CANONICAL_NAME_EX:9

This element is the same as <b>DS_CANONICAL_NAME</b> except that the rightmost forward slash (/) is replaced with a newline character (\n), even in a domain-only case. For example:

engineering.fabrikam.com/software\nsomeone

### -field DS_SERVICE_PRINCIPAL_NAME:10

Indicates it is using a generalized service principal name. For example:

www/www.fabrikam.com@fabrikam.com

### -field DS_SID_OR_SID_HISTORY_NAME:11

Indicates a Security Identifier (SID) for the object. This can be either the current SID or a SID from the object SID history. The SID string can use either the standard string representation of a SID, or one of the string constants defined in Sddl.h. For more information about converting a binary SID into a SID string, see 
<a href="/windows/desktop/SecAuthZ/sid-strings">SID Strings</a>. The following is an example of a SID string:

S-1-5-21-397955417-626881126-188441444-501

### -field DS_DNS_DOMAIN_NAME:12

Not supported by the Directory Service (DS) APIs.

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
