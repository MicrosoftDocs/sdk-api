---
UID: NS:resapi.GET_OPERATION_CONTEXT_PARAMS
title: GET_OPERATION_CONTEXT_PARAMS
author: windows-sdk-content
description: Represents context parameters that are used as input for the CLUSCTL_RESOURCE_GET_OPERATION_CONTEXT control code.
old-location: mscs\get_operation_context_params.htm
old-project: MsCS
ms.assetid: 682215D9-7965-46D5-ABC7-A37B685C43F5
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PGET_OPERATION_CONTEXT_PARAMS, GET_OPERATION_CONTEXT_PARAMS, GET_OPERATION_CONTEXT_PARAMS structure [Failover Cluster], PGET_OPERATION_CONTEXT_PARAMS, PGET_OPERATION_CONTEXT_PARAMS structure pointer [Failover Cluster], mscs.get_operation_context_params, resapi/GET_OPERATION_CONTEXT_PARAMS, resapi/PGET_OPERATION_CONTEXT_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: GET_OPERATION_CONTEXT_PARAMS, *PGET_OPERATION_CONTEXT_PARAMS
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - GET_OPERATION_CONTEXT_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# GET_OPERATION_CONTEXT_PARAMS structure


## -description


Represents context parameters that are used as input for the <a href="https://msdn.microsoft.com/BCB58D8A-5FF6-46BD-8144-919C6DB44593">CLUSCTL_RESOURCE_GET_OPERATION_CONTEXT</a> control code.


## -struct-fields




### -field Size

The size of this structure, in bytes.


### -field Version

The version of this structure.


### -field Type

A  <a href="https://msdn.microsoft.com/8C074E15-4060-4AC7-BB59-959854102EE0">RESDLL_CONTEXT_OPERATION_TYPE</a> enumeration value that specifies the context operation type.


### -field Priority

TBD


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

