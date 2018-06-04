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
 

 

