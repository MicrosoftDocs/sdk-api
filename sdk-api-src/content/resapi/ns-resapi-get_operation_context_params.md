---
UID: NS:resapi.GET_OPERATION_CONTEXT_PARAMS
title: GET_OPERATION_CONTEXT_PARAMS (resapi.h)
description: Represents context parameters that are used as input for the CLUSCTL_RESOURCE_GET_OPERATION_CONTEXT control code.
helpviewer_keywords: ["*PGET_OPERATION_CONTEXT_PARAMS","GET_OPERATION_CONTEXT_PARAMS","GET_OPERATION_CONTEXT_PARAMS structure [Failover Cluster]","PGET_OPERATION_CONTEXT_PARAMS","PGET_OPERATION_CONTEXT_PARAMS structure pointer [Failover Cluster]","mscs.get_operation_context_params","resapi/GET_OPERATION_CONTEXT_PARAMS","resapi/PGET_OPERATION_CONTEXT_PARAMS"]
old-location: mscs\get_operation_context_params.htm
tech.root: MsCS
ms.assetid: 682215D9-7965-46D5-ABC7-A37B685C43F5
ms.date: 12/05/2018
ms.keywords: '*PGET_OPERATION_CONTEXT_PARAMS, GET_OPERATION_CONTEXT_PARAMS, GET_OPERATION_CONTEXT_PARAMS structure [Failover Cluster], PGET_OPERATION_CONTEXT_PARAMS, PGET_OPERATION_CONTEXT_PARAMS structure pointer [Failover Cluster], mscs.get_operation_context_params, resapi/GET_OPERATION_CONTEXT_PARAMS, resapi/PGET_OPERATION_CONTEXT_PARAMS'
f1_keywords:
- resapi/GET_OPERATION_CONTEXT_PARAMS
dev_langs:
- c++
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
- kbSyntax
api_type:
- <TBD>
api_location:
- 
api_name:
- GET_OPERATION_CONTEXT_PARAMS
targetos: Windows
req.typenames: GET_OPERATION_CONTEXT_PARAMS, *PGET_OPERATION_CONTEXT_PARAMS
req.redist: 
ms.custom: 19H1
---

# GET_OPERATION_CONTEXT_PARAMS structure


## -description


Represents context parameters that are used as input for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/clusctl-resource-get-operation-context">CLUSCTL_RESOURCE_GET_OPERATION_CONTEXT</a> control code.


## -struct-fields




### -field Size

The size of this structure, in bytes.


### -field Version

The version of this structure.


### -field Type

A  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/ne-resapi-resdll_context_operation_type">RESDLL_CONTEXT_OPERATION_TYPE</a> enumeration value that specifies the context operation type.


### -field Priority

TBD


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>
 

 

