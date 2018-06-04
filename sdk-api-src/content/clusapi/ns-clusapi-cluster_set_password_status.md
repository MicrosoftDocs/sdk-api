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

# CLUSTER_SET_PASSWORD_STATUS structure


## -description


Used by the 
    <a href="https://msdn.microsoft.com/4afadb62-2bea-46ef-b0d6-e327ac96d16f">SetClusterServiceAccountPassword</a> 
    function to return the results of a <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> user 
    account password change for each cluster node.


## -struct-fields




### -field NodeId

Identifies the node on which the password change attempt was made.


### -field SetAttempted

If <b>TRUE</b>, indicates that the password change was attempted on this node.


### -field ReturnStatus

An error code describing the results of the password change.

