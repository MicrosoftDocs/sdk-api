---
UID: NE:resapi.RESDLL_CONTEXT_OPERATION_TYPE
title: RESDLL_CONTEXT_OPERATION_TYPE (resapi.h)
description: Specifies the various types of context operations for the GET_OPERATION_CONTEXT_PARAMS structure.
helpviewer_keywords: ["*PRESDLL_CONTEXT_OPERATION_TYPE","PRESDLL_CONTEXT_OPERATION_TYPE","PRESDLL_CONTEXT_OPERATION_TYPE enumeration pointer [Failover Cluster]","RESDLL_CONTEXT_OPERATION_TYPE","RESDLL_CONTEXT_OPERATION_TYPE enumeration [Failover Cluster]","ResdllContextOperationTypeDrain","ResdllContextOperationTypeDrainFailure","ResdllContextOperationTypeEmbeddedFailure","ResdllContextOperationTypeFailback","ResdllContextOperationTypeNetworkDisconnect","ResdllContextOperationTypeNetworkDisconnectMoveRetry","ResdllContextOperationTypePreemption","mscs.resdll_context_operation_type","resapi/PRESDLL_CONTEXT_OPERATION_TYPE","resapi/RESDLL_CONTEXT_OPERATION_TYPE","resapi/ResdllContextOperationTypeDrain","resapi/ResdllContextOperationTypeDrainFailure","resapi/ResdllContextOperationTypeEmbeddedFailure","resapi/ResdllContextOperationTypeFailback","resapi/ResdllContextOperationTypeNetworkDisconnect","resapi/ResdllContextOperationTypeNetworkDisconnectMoveRetry","resapi/ResdllContextOperationTypePreemption"]
old-location: mscs\resdll_context_operation_type.htm
tech.root: MsCS
ms.assetid: 8C074E15-4060-4AC7-BB59-959854102EE0
ms.date: 12/05/2018
ms.keywords: '*PRESDLL_CONTEXT_OPERATION_TYPE, PRESDLL_CONTEXT_OPERATION_TYPE, PRESDLL_CONTEXT_OPERATION_TYPE enumeration pointer [Failover Cluster], RESDLL_CONTEXT_OPERATION_TYPE, RESDLL_CONTEXT_OPERATION_TYPE enumeration [Failover Cluster], ResdllContextOperationTypeDrain, ResdllContextOperationTypeDrainFailure, ResdllContextOperationTypeEmbeddedFailure, ResdllContextOperationTypeFailback, ResdllContextOperationTypeNetworkDisconnect, ResdllContextOperationTypeNetworkDisconnectMoveRetry, ResdllContextOperationTypePreemption, mscs.resdll_context_operation_type, resapi/PRESDLL_CONTEXT_OPERATION_TYPE, resapi/RESDLL_CONTEXT_OPERATION_TYPE, resapi/ResdllContextOperationTypeDrain, resapi/ResdllContextOperationTypeDrainFailure, resapi/ResdllContextOperationTypeEmbeddedFailure, resapi/ResdllContextOperationTypeFailback, resapi/ResdllContextOperationTypeNetworkDisconnect, resapi/ResdllContextOperationTypeNetworkDisconnectMoveRetry, resapi/ResdllContextOperationTypePreemption'
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
targetos: Windows
req.typenames: RESDLL_CONTEXT_OPERATION_TYPE, *PRESDLL_CONTEXT_OPERATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESDLL_CONTEXT_OPERATION_TYPE
 - resapi/RESDLL_CONTEXT_OPERATION_TYPE
 - PRESDLL_CONTEXT_OPERATION_TYPE
 - resapi/PRESDLL_CONTEXT_OPERATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - RESDLL_CONTEXT_OPERATION_TYPE
---

# RESDLL_CONTEXT_OPERATION_TYPE enumeration


## -description

Specifies the various types of context operations for the <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-get_operation_context_params">GET_OPERATION_CONTEXT_PARAMS</a> structure.

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

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>