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

# DS_SITE_COST_INFO structure


## -description


The <b>DS_SITE_COST_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a> function to contain communication cost data.


## -struct-fields




### -field errorCode

Contains a success or error code that indicates if the cost data for the site could  be obtained. This member can contain one of the following values.



#### ERROR_SUCCESS

The communication cost of the site was obtained and is contained in the <b>cost</b> member of this structure.



#### ERROR_DS_OBJ_NOT_FOUND

The communication cost of the site cannot be obtained. The <b>cost</b> member of this structure should be ignored.


### -field cost

If the <b>errorCode</b> member contains <b>ERROR_SUCCESS</b>, this member contains the communication cost value of the site. If the <b>errorCode</b> member contains <b>ERROR_DS_OBJ_NOT_FOUND</b>, this contents of this member is undefined.


## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">DC and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a>
 

 

