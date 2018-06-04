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

# DS_NAME_FLAGS enumeration


## -description


The <b>DS_NAME_FLAGS</b> enumeration is used to define how the name syntax will be cracked. These flags are used by the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function.


## -enum-fields




### -field DS_NAME_NO_FLAGS

Indicates that there are no associated flags.


### -field DS_NAME_FLAG_SYNTACTICAL_ONLY

Performs a syntactical mapping at the client without transferring over the network. The only syntactic mapping supported is from <a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_FQDN_1779_NAME</a> to <b>DS_CANONICAL_NAME</b> or <b>DS_CANONICAL_NAME_EX</b>. <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> returns the <b>DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING</b> flag if a  syntactical mapping is not possible.


### -field DS_NAME_FLAG_EVAL_AT_DC

Forces a trip to the domain controller for evaluation, even if the syntax could be cracked locally.


### -field DS_NAME_FLAG_GCVERIFY

The call fails if the domain controller is not a global catalog server.


### -field DS_NAME_FLAG_TRUST_REFERRAL

Enables cross forest trust referral.


## -see-also




<a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_NAME_FORMAT</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

