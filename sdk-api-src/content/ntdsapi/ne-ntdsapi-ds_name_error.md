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

# DS_NAME_ERROR enumeration


## -description


The <b>DS_NAME_ERROR</b> enumeration defines the errors returned by the <b>status</b> member of the <a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a> structure. These are potential errors that may be encountered while a name is converted by the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function.


## -enum-fields




### -field DS_NAME_NO_ERROR

The conversion was successful.


### -field DS_NAME_ERROR_RESOLVING

A generic processing error occurred.


### -field DS_NAME_ERROR_NOT_FOUND

The name cannot be found or the caller does not have permission to access the name.


### -field DS_NAME_ERROR_NOT_UNIQUE

The input name is mapped to more than one output name or the desired format did not have a single, unique value for the object found.


### -field DS_NAME_ERROR_NO_MAPPING

The input name was found, but the associated output format cannot be found. This can occur if the object does not have all the required attributes.


### -field DS_NAME_ERROR_DOMAIN_ONLY

Unable to resolve entire name, but was able to determine in which domain object resides. The caller is expected to retry the call at a domain controller for the specified domain. The entire name cannot be resolved, but the domain that the object resides in could be determined. The <b>pDomain</b> member of the <a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a> contains valid data when this error is specified.


### -field DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING

A syntactical mapping cannot be performed on the client without transmitting over the network.


### -field DS_NAME_ERROR_TRUST_REFERRAL

The name is from an external trusted forest.


## -see-also




<a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

