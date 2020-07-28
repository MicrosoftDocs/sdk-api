---
UID: NE:secext.__unnamed_enum_0
title: EXTENDED_NAME_FORMAT (secext.h)
description: Specifies a format for a directory service object name.
helpviewer_keywords: ["*PEXTENDED_NAME_FORMAT","EXTENDED_NAME_FORMAT","EXTENDED_NAME_FORMAT enumeration","NameCanonical","NameCanonicalEx","NameDisplay","NameDnsDomain","NameFullyQualifiedDN","NameSamCompatible","NameServicePrincipal","NameUniqueId","NameUnknown","NameUserPrincipal","PEXTENDED_NAME_FORMAT","PEXTENDED_NAME_FORMAT enumeration pointer","_win32_extended_name_format_str","base.extended_name_format_str","secext/EXTENDED_NAME_FORMAT","secext/NameCanonical","secext/NameCanonicalEx","secext/NameDisplay","secext/NameDnsDomain","secext/NameFullyQualifiedDN","secext/NameSamCompatible","secext/NameServicePrincipal","secext/NameUniqueId","secext/NameUnknown","secext/NameUserPrincipal","secext/PEXTENDED_NAME_FORMAT"]
old-location: base\extended_name_format_str.htm
tech.root: winprog
ms.assetid: 1270c412-2fa5-4f5d-a86e-1ab3146c6683
ms.date: 12/05/2018
ms.keywords: '*PEXTENDED_NAME_FORMAT, EXTENDED_NAME_FORMAT, EXTENDED_NAME_FORMAT enumeration, NameCanonical, NameCanonicalEx, NameDisplay, NameDnsDomain, NameFullyQualifiedDN, NameSamCompatible, NameServicePrincipal, NameUniqueId, NameUnknown, NameUserPrincipal, PEXTENDED_NAME_FORMAT, PEXTENDED_NAME_FORMAT enumeration pointer, _win32_extended_name_format_str, base.extended_name_format_str, secext/EXTENDED_NAME_FORMAT, secext/NameCanonical, secext/NameCanonicalEx, secext/NameDisplay, secext/NameDnsDomain, secext/NameFullyQualifiedDN, secext/NameSamCompatible, secext/NameServicePrincipal, secext/NameUniqueId, secext/NameUnknown, secext/NameUserPrincipal, secext/PEXTENDED_NAME_FORMAT'
f1_keywords:
- secext/EXTENDED_NAME_FORMAT
dev_langs:
- c++
req.header: secext.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Secext.h
api_name:
- EXTENDED_NAME_FORMAT
targetos: Windows
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
req.redist: 
ms.custom: 19H1
---

# EXTENDED_NAME_FORMAT enumeration


## -description


Specifies a format for a directory service object name.


## -enum-fields




### -field NameUnknown

An unknown name type.


### -field NameFullyQualifiedDN

The fully qualified distinguished name (for example, CN=Jeff Smith,OU=Users,DC=Engineering,DC=Microsoft,DC=Com).


### -field NameSamCompatible

A legacy account name (for example, Engineering\JSmith). The domain-only version includes trailing backslashes (\\).


### -field NameDisplay

A "friendly" display name (for example, Jeff Smith). The display name is not necessarily the defining relative distinguished name (RDN).


### -field NameUniqueId

A GUID string that the 
<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-iidfromstring">IIDFromString</a> function returns (for example, {4fa050f0-f561-11cf-bdd9-00aa003a77b6}).


### -field NameCanonical

The complete canonical name (for example, engineering.microsoft.com/software/someone). The domain-only version includes a trailing forward slash (/).


### -field NameUserPrincipal

The user principal name (for example, someone@example.com).


### -field NameCanonicalEx

The same as NameCanonical except that the rightmost forward slash (/) is replaced with a new line character (\n), even in a domain-only case (for example, engineering.microsoft.com/software\nJSmith).


### -field NameServicePrincipal

The generalized service principal name (for example, www/www.microsoft.com@microsoft.com).


### -field NameDnsDomain

The DNS domain name followed by a backward-slash and the SAM user name.


### -field NameGivenName


### -field NameSurname




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea">GetComputerObjectName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-translatenamea">TranslateName</a>
 

 

