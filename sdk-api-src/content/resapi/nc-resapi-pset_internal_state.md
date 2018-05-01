---
UID: NC:resapi.PSET_INTERNAL_STATE
title: PSET_INTERNAL_STATE
author: windows-driver-content
description: Sets the internal state of a resource.
old-location: mscs\setinternalstate.htm
old-project: MsCS
ms.assetid: B9ECD98B-D867-44C0-846F-8FE96E44F387
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PSET_INTERNAL_STATE, PSET_INTERNAL_STATE callback function [Failover Cluster], SetInternalState, SetInternalState callback function [Failover Cluster], mscs.setinternalstate, resapi/PSET_INTERNAL_STATE, resapi/SetInternalState
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	SetInternalState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSET_INTERNAL_STATE callback


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

