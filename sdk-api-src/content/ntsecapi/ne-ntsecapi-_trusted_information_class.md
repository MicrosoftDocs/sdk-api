---
UID: NE:ntsecapi._TRUSTED_INFORMATION_CLASS
title: "_TRUSTED_INFORMATION_CLASS"
author: windows-sdk-content
description: The TRUSTED_INFORMATION_CLASS enumeration type defines values that indicate the type of information to set or query for a trusted domain.
old-location: security\trusted_information_class.htm
tech.root: SecMgmt
ms.assetid: 442a0944-b498-4d9f-b338-d5aed1663d8d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PTRUSTED_INFORMATION_CLASS, PTRUSTED_INFORMATION_CLASS, PTRUSTED_INFORMATION_CLASS enumeration pointer [Security], TRUSTED_INFORMATION_CLASS, TRUSTED_INFORMATION_CLASS enumeration [Security], TrustedControllersInformation, TrustedDomainAuthInformation, TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _TRUSTED_INFORMATION_CLASS, _lsa_trusted_information_class, ntsecapi/PTRUSTED_INFORMATION_CLASS, ntsecapi/TRUSTED_INFORMATION_CLASS, ntsecapi/TrustedControllersInformation, ntsecapi/TrustedDomainAuthInformation, ntsecapi/TrustedDomainFullInformation, ntsecapi/TrustedDomainInformationBasic, ntsecapi/TrustedDomainInformationEx, ntsecapi/TrustedDomainNameInformation, ntsecapi/TrustedPasswordInformation, ntsecapi/TrustedPosixOffsetInformation, security.trusted_information_class"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntsecapi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - TRUSTED_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
req.redist: 
---

# _TRUSTED_INFORMATION_CLASS enumeration


## -description


The <b>TRUSTED_INFORMATION_CLASS</b> enumeration type defines values that indicate the type of information to set or query for a trusted domain.

Each value has an associated structure that the 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> and 
<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a> functions use to store the information.


## -enum-fields




### -field TrustedDomainNameInformation

Query or set the name of a trusted domain. Use the 
<a href="https://msdn.microsoft.com/9bc1301b-1d09-4cd2-8590-e7756ee4792d">TRUSTED_DOMAIN_NAME_INFO</a> structure.


### -field TrustedControllersInformation

This value is obsolete.


### -field TrustedPosixOffsetInformation

Query or set the value used to generate Posix user and group identifiers. Use the 
<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a> structure.


### -field TrustedPasswordInformation

This value has been superseded by the <b>TrustedDomainAuthInformation</b> value. 
					


### -field TrustedDomainInformationBasic

This value is obsolete.
					


### -field TrustedDomainInformationEx

Query extended information for a trusted domain. Use the 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.


### -field TrustedDomainAuthInformation

Query authentication information for a trusted domain. Use the 
<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure.


### -field TrustedDomainFullInformation

Query complete information for a trusted domain. This information includes the Posix offset information, authentication information, and the extended information returned for the <b>TrustedDomainInformationEx</b> value. Use the 
<a href="https://msdn.microsoft.com/b7abfe1e-d9e6-4583-a738-c16190ffd44d">TRUSTED_DOMAIN_FULL_INFORMATION</a> structure.


### -field TrustedDomainAuthInformationInternal


### -field TrustedDomainFullInformationInternal


### -field TrustedDomainInformationEx2Internal


### -field TrustedDomainFullInformation2Internal


### -field TrustedDomainSupportedEncryptionTypes




## -see-also




<a href="https://msdn.microsoft.com/2b5e6f79-b97a-4018-a45a-37c300c3dc0d">LSA_TRUST_INFORMATION</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/b7abfe1e-d9e6-4583-a738-c16190ffd44d">TRUSTED_DOMAIN_FULL_INFORMATION</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/9bc1301b-1d09-4cd2-8590-e7756ee4792d">TRUSTED_DOMAIN_NAME_INFO</a>



<a href="https://msdn.microsoft.com/2c3aca10-8efd-4278-8127-2d31db776c0e">TRUSTED_PASSWORD_INFO</a>



<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a>
 

 

