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

# IFsrmFileManagementJob::get_CustomAction


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The action to execute when all the conditions are met.

This property is read-only.


## -parameters


## -remarks



To create the custom action, call the 
    <a href="https://msdn.microsoft.com/886992bd-ca0b-4f21-8036-39703c7c99ba">IFsrmFileManagementJob::CreateCustomAction</a> 
    method.

For a list of macros supported, perform a "get" operation on the 
    <a href="https://msdn.microsoft.com/222c826f-0ade-4e5d-be2e-5c0dfa8758d0">IFsrmFileManagementJobManager::ActionVariables</a> 
    and 
    <a href="https://msdn.microsoft.com/d8e625b2-5fdd-4e7e-8c20-ad6e3e21a918">IFsrmFileManagementJobManager::ActionVariableDescriptions</a> 
    properties.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

