---
UID: NC:resapi.PSET_INTERNAL_STATE
title: PSET_INTERNAL_STATE (resapi.h)
description: Sets the internal state of a resource.
helpviewer_keywords: ["PSET_INTERNAL_STATE","PSET_INTERNAL_STATE callback function [Failover Cluster]","SetInternalState","SetInternalState callback","SetInternalState callback function [Failover Cluster]","mscs.setinternalstate","resapi/PSET_INTERNAL_STATE","resapi/SetInternalState"]
old-location: mscs\setinternalstate.htm
tech.root: MsCS
ms.assetid: B9ECD98B-D867-44C0-846F-8FE96E44F387
ms.date: 12/05/2018
ms.keywords: PSET_INTERNAL_STATE, PSET_INTERNAL_STATE callback function [Failover Cluster], SetInternalState, SetInternalState callback, SetInternalState callback function [Failover Cluster], mscs.setinternalstate, resapi/PSET_INTERNAL_STATE, resapi/SetInternalState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSET_INTERNAL_STATE
 - resapi/PSET_INTERNAL_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetInternalState
---

# PSET_INTERNAL_STATE callback function


## -description

Sets the internal state of a resource

## -parameters

### -param unnamedParam1

### -param stateType [in]

A <a href="/previous-versions/windows/desktop/api/resapi/ne-resapi-cluster_resource_application_state">CLUSTER_RESOURCE_APPLICATION_STATE</a> value

### -param active [in]

Whether the resource is active


#### - [in]

A resource handle