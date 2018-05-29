---
UID: NS:ntsecapi._TRUSTED_DOMAIN_AUTH_INFORMATION
title: "_TRUSTED_DOMAIN_AUTH_INFORMATION"
author: windows-sdk-content
description: The TRUSTED_DOMAIN_AUTH_INFORMATION structure is used to retrieve authentication information for a trusted domain. The LsaQueryTrustedDomainInfo function uses this structure when its InformationClass parameter is set to TrustedDomainAuthInformation.
old-location: security\trusted_domain_auth_information.htm
old-project: SecMgmt
ms.assetid: 2ec606d7-42bd-47cc-a4cd-82908774aa43
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PTRUSTED_DOMAIN_AUTH_INFORMATION, PTRUSTED_DOMAIN_AUTH_INFORMATION, PTRUSTED_DOMAIN_AUTH_INFORMATION structure pointer [Security], TRUSTED_DOMAIN_AUTH_INFORMATION, TRUSTED_DOMAIN_AUTH_INFORMATION structure [Security], _TRUSTED_DOMAIN_AUTH_INFORMATION, _lsa_trusted_domain_auth_information, ntsecapi/PTRUSTED_DOMAIN_AUTH_INFORMATION, ntsecapi/TRUSTED_DOMAIN_AUTH_INFORMATION, security.trusted_domain_auth_information"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: TRUSTED_DOMAIN_AUTH_INFORMATION, *PTRUSTED_DOMAIN_AUTH_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	TRUSTED_DOMAIN_AUTH_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _TRUSTED_DOMAIN_AUTH_INFORMATION structure


## -description


The <b>TRUSTED_DOMAIN_AUTH_INFORMATION</b> structure is used to retrieve authentication information for a trusted domain. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> function uses this structure when its <i>InformationClass</i> parameter is set to <b>TrustedDomainAuthInformation</b>.


## -struct-fields




### -field IncomingAuthInfos

Specifies the number of entries in the <b>IncomingAuthenticationInformation</b> and <b>IncomingPreviousAuthenticationInformation</b> arrays.


### -field IncomingAuthenticationInformation

Pointer to an array of 
<a href="https://msdn.microsoft.com/61c17831-4a82-4766-b5af-e97a6d467462">LSA_AUTH_INFORMATION</a> structures containing the authentication information for the incoming side of a trust relationship.


### -field IncomingPreviousAuthenticationInformation

Pointer to an array of <a href="https://msdn.microsoft.com/61c17831-4a82-4766-b5af-e97a6d467462">LSA_AUTH_INFORMATION</a> structures containing the previous authentication information (or old password) for the incoming side of a trust relationship. There must be one of these for every entry in the <b>IncomingAuthenticationInformation</b> array.


### -field OutgoingAuthInfos

Specifies the number of entries in the <b>OutgoingAuthenticationInformation</b> and <b>OutgoingPreviousAuthenticationInformation</b> arrays.


### -field OutgoingAuthenticationInformation

Pointer to an array of <a href="https://msdn.microsoft.com/61c17831-4a82-4766-b5af-e97a6d467462">LSA_AUTH_INFORMATION</a> structures containing the authentication information for the outgoing side of a trust relationship.


### -field OutgoingPreviousAuthenticationInformation

Pointer to an array of <a href="https://msdn.microsoft.com/61c17831-4a82-4766-b5af-e97a6d467462">LSA_AUTH_INFORMATION</a> structures containing the previous authentication information (or old password) for the outgoing side of a trust relationship. There must be one of these for every entry in the <b>OutgoingAuthenticationInformation</b> array.


## -see-also




<a href="https://msdn.microsoft.com/61c17831-4a82-4766-b5af-e97a6d467462">LSA_AUTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/2f458098-9498-4f08-bd13-ac572678d734">LsaCreateTrustedDomainEx</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/d33d6cee-bd8b-49f4-8e65-07cdc65bec7c">LsaQueryTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/263e1025-1010-463d-8bc7-cdf916ce9872">LsaSetTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

