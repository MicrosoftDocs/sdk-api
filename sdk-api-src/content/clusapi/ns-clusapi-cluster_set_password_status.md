---
UID: NS:clusapi.CLUSTER_SET_PASSWORD_STATUS
title: CLUSTER_SET_PASSWORD_STATUS
author: windows-sdk-content
description: Used by the SetClusterServiceAccountPassword function to return the results of a Cluster service user account password change for each cluster node.
old-location: mscs\cluster_set_password_status.htm
tech.root: mscs
ms.assetid: a9e0e99f-b57b-4bf1-93d5-6f09d907aed1
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: "*PCLUSTER_SET_PASSWORD_STATUS, CLUSTER_SET_PASSWORD_STATUS, CLUSTER_SET_PASSWORD_STATUS structure [Failover Cluster], PCLUSTER_SET_PASSWORD_STATUS, PCLUSTER_SET_PASSWORD_STATUS structure pointer [Failover Cluster], _wolf_cluster_set_password_status, clusapi/CLUSTER_SET_PASSWORD_STATUS, clusapi/PCLUSTER_SET_PASSWORD_STATUS, mscs.cluster_set_password_status"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SET_PASSWORD_STATUS
product: Windows
targetos: Windows
req.typenames: CLUSTER_SET_PASSWORD_STATUS, *PCLUSTER_SET_PASSWORD_STATUS
req.redist: 
---

# CLUSTER_SET_PASSWORD_STATUS structure


## -description


Used by the 
    <a href="https://msdn.microsoft.com/4afadb62-2bea-46ef-b0d6-e327ac96d16f">SetClusterServiceAccountPassword</a> 
    function to return the results of a <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> user 
    account password change for each cluster node.


## -struct-fields




### -field NodeId

Identifies the node on which the password change attempt was made.


### -field SetAttempted

If <b>TRUE</b>, indicates that the password change was attempted on this node.


### -field ReturnStatus

An error code describing the results of the password change.

