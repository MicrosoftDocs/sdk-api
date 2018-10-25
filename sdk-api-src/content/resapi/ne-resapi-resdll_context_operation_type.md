---
UID: NE:resapi.RESDLL_CONTEXT_OPERATION_TYPE
title: RESDLL_CONTEXT_OPERATION_TYPE
author: windows-sdk-content
description: Specifies the various types of context operations for the GET_OPERATION_CONTEXT_PARAMS structure.
old-location: mscs\resdll_context_operation_type.htm
tech.root: mscs
ms.assetid: 8C074E15-4060-4AC7-BB59-959854102EE0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PRESDLL_CONTEXT_OPERATION_TYPE, PRESDLL_CONTEXT_OPERATION_TYPE, PRESDLL_CONTEXT_OPERATION_TYPE enumeration pointer [Failover Cluster], RESDLL_CONTEXT_OPERATION_TYPE, RESDLL_CONTEXT_OPERATION_TYPE enumeration [Failover Cluster], ResdllContextOperationTypeDrain, ResdllContextOperationTypeDrainFailure, ResdllContextOperationTypeEmbeddedFailure, ResdllContextOperationTypeFailback, ResdllContextOperationTypeNetworkDisconnect, ResdllContextOperationTypeNetworkDisconnectMoveRetry, ResdllContextOperationTypePreemption, mscs.resdll_context_operation_type, resapi/PRESDLL_CONTEXT_OPERATION_TYPE, resapi/RESDLL_CONTEXT_OPERATION_TYPE, resapi/ResdllContextOperationTypeDrain, resapi/ResdllContextOperationTypeDrainFailure, resapi/ResdllContextOperationTypeEmbeddedFailure, resapi/ResdllContextOperationTypeFailback, resapi/ResdllContextOperationTypeNetworkDisconnect, resapi/ResdllContextOperationTypeNetworkDisconnectMoveRetry, resapi/ResdllContextOperationTypePreemption"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ResApi.h
api_name:
 - RESDLL_CONTEXT_OPERATION_TYPE
product: Windows
targetos: Windows
req.typenames: RESDLL_CONTEXT_OPERATION_TYPE, *PRESDLL_CONTEXT_OPERATION_TYPE
req.redist: 
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
 

 

