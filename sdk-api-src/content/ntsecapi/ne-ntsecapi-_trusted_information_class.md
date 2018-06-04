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
 

 

