---
UID: NC:resapi.PSET_INTERNAL_STATE
title: PSET_INTERNAL_STATE
author: windows-sdk-content
description: Sets the internal state of a resource.
old-location: mscs\setinternalstate.htm
tech.root: mscs
ms.assetid: B9ECD98B-D867-44C0-846F-8FE96E44F387
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PSET_INTERNAL_STATE, PSET_INTERNAL_STATE callback function [Failover Cluster], SetInternalState, SetInternalState callback, SetInternalState callback function [Failover Cluster], mscs.setinternalstate, resapi/PSET_INTERNAL_STATE, resapi/SetInternalState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetInternalState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSET_INTERNAL_STATE callback function


## -description


Sets the internal state of a resource


## -parameters




### -param Arg1


### -param stateType [in]

A <a href="https://msdn.microsoft.com/A67B8251-214B-44DD-8166-C0F74335CE1F">CLUSTER_RESOURCE_APPLICATION_STATE</a> value


### -param active [in]

Whether the resource is active


#### - [in]

A resource handle

