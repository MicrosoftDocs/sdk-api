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

# DsGetDomainControllerInfoA function


## -description


The <b>DsGetDomainControllerInfo</b> function retrieves data about the domain controllers in a domain.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param DomainName [in]

Pointer to a null-terminated string that specifies the domain name.


### -param InfoLevel [in]

Contains a value that indicates the version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure to  return. This can be one of the following values.



#### 1

The function provides the domain data in the <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a> structure format.



#### 2

The function provides the domain data in the <a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a> structure format.



#### 3

The function provides the domain data in the <a href="https://msdn.microsoft.com/510f458e-4c08-41c7-b290-1372ac9c8beb">DS_DOMAIN_CONTROLLER_INFO_3</a> structure format.


### -param pcOut [out]

Pointer to a <b>DWORD</b> variable that receives the number of items returned in <i>ppInfo</i> array.


### -param ppInfo [out]

Pointer to a pointer variable that receives an array of  <b>DS_DOMAIN_CONTROLLER_INFO_*</b> structures. The type of structures in this array is defined by the <i>InfoLevel</i> parameter. The caller must free this array, when it is no longer required, by using 
the <a href="https://msdn.microsoft.com/1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2">DsFreeDomainControllerInfo</a> function.


## -returns



If the function returns domain controller data, the return value is <b>ERROR_SUCCESS</b>. If the caller does not have the privileges to access the server objects, the return value is <b>ERROR_SUCCESS</b>, but the <b>DS_DOMAIN_CONTROLLER_INFO</b> structures could be empty.

If the function fails, the return value can be one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a>



<a href="https://msdn.microsoft.com/510f458e-4c08-41c7-b290-1372ac9c8beb">DS_DOMAIN_CONTROLLER_INFO_3</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2">DsFreeDomainControllerInfo</a>
 

 

