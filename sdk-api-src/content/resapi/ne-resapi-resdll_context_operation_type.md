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

# RESDLL_CONTEXT_OPERATION_TYPE enumeration


## -description


Specifies the various types of context operations for the <a href="https://msdn.microsoft.com/682215D9-7965-46D5-ABC7-A37B685C43F5">GET_OPERATION_CONTEXT_PARAMS</a> structure.


## -enum-fields




### -field ResdllContextOperationTypeFailback

A group fail back.


### -field ResdllContextOperationTypeDrain

A node drain.


### -field ResdllContextOperationTypeDrainFailure

A node drain failure.


### -field ResdllContextOperationTypeEmbeddedFailure

An embedded failure.


### -field ResdllContextOperationTypePreemption

A preemption failure.


### -field ResdllContextOperationTypeNetworkDisconnect

A network connection failure.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.


### -field ResdllContextOperationTypeNetworkDisconnectMoveRetry

A network connection was disconnected and it is being re-established.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

