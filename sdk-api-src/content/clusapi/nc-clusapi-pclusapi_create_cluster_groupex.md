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

# PCLUSAPI_CREATE_CLUSTER_GROUPEX callback function


## -description


Creates a new cluster group with the options specified in the <b>CLUSTER_CREATE_GROUP_INFO</b> structure in a single operation.
   The <b>PCLUSAPI_CREATE_CLUSTER_GROUPEX</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

The handle to the cluster in which the group will be created.


### -param lpszGroupName [in]

The name of the new cluster group.


### -param pGroupInfo [in, optional]

The additional information used to create the group.


## -returns



If the operation is successful, the function returns a handle to the newly created group.
If the operation fails, the function returns <b>NULL</b>.




## -remarks



The <b>CLUSTER_CREATE_GROUP_INFO</b> structure enables additional properties for group creation.  Currently, only the group type can be specified, which  enables the group type to be set when the group is created.



