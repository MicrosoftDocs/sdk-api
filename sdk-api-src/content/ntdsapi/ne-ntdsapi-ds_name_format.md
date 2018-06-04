---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DS_NAME_FORMAT enumeration


## -description


The <b>DS_NAME_FORMAT</b> enumeration provides formats to use for input and output names for the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function.


## -enum-fields




### -field DS_UNKNOWN_NAME

Indicates the name is using an unknown name type. This format can impact performance because it forces the server to attempt to match all possible
    formats. Only use this value if the input format is unknown.


### -field DS_FQDN_1779_NAME

Indicates that the fully qualified distinguished name is used. For example:

CN=someone,OU=Users,DC=Engineering,DC=Fabrikam,DC=Com


### -field DS_NT4_ACCOUNT_NAME

Indicates a Windows NT 4.0 account name. For example:

Engineering\someone

The domain-only version includes two trailing backslashes (\\).


### -field DS_DISPLAY_NAME

Indicates a user-friendly display name, for example, Jeff Smith. The display name is not necessarily the same as relative distinguished name (RDN).


### -field DS_UNIQUE_ID_NAME

Indicates a GUID string that the <a href="_com_iidfromstring">IIDFromString</a> function returns. For example:

{4fa050f0-f561-11cf-bdd9-00aa003a77b6}


### -field DS_CANONICAL_NAME

Indicates a complete canonical name. For example:

engineering.fabrikam.com/software/someone

The domain-only version includes a trailing forward slash (/).


### -field DS_USER_PRINCIPAL_NAME

Indicates that it is using the user principal name (UPN). For example:

someone@engineering.fabrikam.com


### -field DS_CANONICAL_NAME_EX

This element is the same as <b>DS_CANONICAL_NAME</b> except that the rightmost forward slash (/) is replaced with a newline character (\n), even in a domain-only case. For example:

engineering.fabrikam.com/software\nsomeone


### -field DS_SERVICE_PRINCIPAL_NAME

Indicates it is using a generalized service principal name. For example:

www/www.fabrikam.com@fabrikam.com


### -field DS_SID_OR_SID_HISTORY_NAME

Indicates a Security Identifier (SID) for the object. This can be either the current SID or a SID from the object SID history. The SID string can use either the standard string representation of a SID, or one of the string constants defined in Sddl.h. For more information about converting a binary SID into a SID string, see 
<a href="https://msdn.microsoft.com/a531532f-afba-46a1-8576-90d4ff881b94">SID Strings</a>. The following is an example of a SID string:

S-1-5-21-397955417-626881126-188441444-501


### -field DS_DNS_DOMAIN_NAME

Not supported by the Directory Service (DS) APIs.


## -see-also




<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

