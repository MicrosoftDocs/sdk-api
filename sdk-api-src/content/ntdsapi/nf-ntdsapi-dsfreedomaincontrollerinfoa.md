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

# DsFreeDomainControllerInfoA function


## -description


The <b>DsFreeDomainControllerInfo</b> function frees memory that is allocated by 
<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> for data about the domain controllers in a domain.


## -parameters




### -param InfoLevel [in]

Indicates what version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure should be freed. This parameter can be one of the following values.



#### 1

The function frees the structure that contains  <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a> data.



#### 2

The function frees the structure that contains <a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a> data.


### -param cInfo [in]

Indicates the number of items in <i>pInfo</i>.


### -param pInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO</a> structures to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a>
 

 

