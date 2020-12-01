---
UID: NE:resapi._RESOURCE_EXIT_STATE
title: RESOURCE_EXIT_STATE (resapi.h)
description: Enumerates the possible exit states of a resource.
helpviewer_keywords: ["RESOURCE_EXIT_STATE","RESOURCE_EXIT_STATE enumeration [Failover Cluster]","ResourceExitStateContinue","ResourceExitStateMax","ResourceExitStateTerminate","mscs.resource_exit_state","resapi/RESOURCE_EXIT_STATE","resapi/ResourceExitStateContinue","resapi/ResourceExitStateMax","resapi/ResourceExitStateTerminate"]
old-location: mscs\resource_exit_state.htm
tech.root: MsCS
ms.assetid: d1b9fd8f-7d49-4396-8f0c-6db8fad5749e
ms.date: 12/05/2018
ms.keywords: RESOURCE_EXIT_STATE, RESOURCE_EXIT_STATE enumeration [Failover Cluster], ResourceExitStateContinue, ResourceExitStateMax, ResourceExitStateTerminate, mscs.resource_exit_state, resapi/RESOURCE_EXIT_STATE, resapi/ResourceExitStateContinue, resapi/ResourceExitStateMax, resapi/ResourceExitStateTerminate
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: RESOURCE_EXIT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RESOURCE_EXIT_STATE
 - resapi/_RESOURCE_EXIT_STATE
 - RESOURCE_EXIT_STATE
 - resapi/RESOURCE_EXIT_STATE
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
 - RESOURCE_EXIT_STATE
---

# RESOURCE_EXIT_STATE enumeration


## -description

Enumerates the possible exit states of a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. These values are returned by the 
    <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a> callback function.

## -enum-fields

### -field ResourceExitStateContinue

The resource has not been terminated. Worker threads may continue 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> and 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> operations for the resource.

### -field ResourceExitStateTerminate

The resource has been terminated. Callers should end 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> operations and immediately terminate all worker 
       threads assigned to the resource.

### -field ResourceExitStateMax

This value is only used for comparisons. All supported values are less than 
      <b>ResourceExitStateMax</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a>