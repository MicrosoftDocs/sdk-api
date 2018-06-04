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

# PCLUSTER_SET_ACCOUNT_ACCESS callback function


## -description


Updates an account access list (ACL) for a cluster.


## -parameters




### -param hCluster [in]

A handle to the cluster.


### -param szAccountSID [in]

The security identifier (SID) or the account name for the new account access entry (ACE).


### -param dwAccess [in]

The access rights controlled by the ACE.


The possible values are:





#### CLUSAPI_READ_ACCESS (0x00000001L)

Read access.



#### CLUSAPI_CHANGE_ACCESS (0x00000002L)

The account can be used to make changes to the cluster.



#### CLUSAPI_NO_ACCESS (0x00000004L)

No access.



#### CLUSAPI_ALL_ACCESS ((CLUSAPI_READ_ACCESS | CLUSAPI_CHANGE_ACCESS))

The account can be used to read and change the cluster.


### -param dwControlType [in]

The  ACE type to use.


The possible values are:





#### CLUSTER_SET_ACCESS_TYPE_ALLOWED (0)

Adds an allowed ACE.



#### CLUSTER_SET_ACCESS_TYPE_DENIED (1)

Adds a denied ACE.



#### CLUSTER_DELETE_ACCESS_CONTROL_ENTRY (2)

Deletes all the ACEs for for the SID.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

