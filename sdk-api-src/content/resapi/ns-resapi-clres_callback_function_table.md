---
UID: NS:resapi.CLRES_CALLBACK_FUNCTION_TABLE
title: CLRES_CALLBACK_FUNCTION_TABLE (resapi.h)
description: Represents a function table for the StartupEx callback function.
helpviewer_keywords: ["*PCLRES_CALLBACK_FUNCTION_TABLE","CLRES_CALLBACK_FUNCTION_TABLE","CLRES_CALLBACK_FUNCTION_TABLE structure [Failover Cluster]","PCLRES_CALLBACK_FUNCTION_TABLE","PCLRES_CALLBACK_FUNCTION_TABLE structure pointer [Failover Cluster]","mscs.clres_callback_function_table","resapi/CLRES_CALLBACK_FUNCTION_TABLE","resapi/PCLRES_CALLBACK_FUNCTION_TABLE"]
old-location: mscs\clres_callback_function_table.htm
tech.root: MsCS
ms.assetid: 1B67B70B-330D-4BA5-AA6C-408588868C76
ms.date: 12/05/2018
ms.keywords: '*PCLRES_CALLBACK_FUNCTION_TABLE, CLRES_CALLBACK_FUNCTION_TABLE, CLRES_CALLBACK_FUNCTION_TABLE structure [Failover Cluster], PCLRES_CALLBACK_FUNCTION_TABLE, PCLRES_CALLBACK_FUNCTION_TABLE structure pointer [Failover Cluster], mscs.clres_callback_function_table, resapi/CLRES_CALLBACK_FUNCTION_TABLE, resapi/PCLRES_CALLBACK_FUNCTION_TABLE'
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
req.typenames: CLRES_CALLBACK_FUNCTION_TABLE, *PCLRES_CALLBACK_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLRES_CALLBACK_FUNCTION_TABLE
 - resapi/CLRES_CALLBACK_FUNCTION_TABLE
 - PCLRES_CALLBACK_FUNCTION_TABLE
 - resapi/PCLRES_CALLBACK_FUNCTION_TABLE
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
 - CLRES_CALLBACK_FUNCTION_TABLE
---

# CLRES_CALLBACK_FUNCTION_TABLE structure


## -description

Represents a function table for the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_ex_routine">StartupEx</a> callback function.

## -struct-fields

### -field LogEvent

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point.

### -field SetResourceStatusEx

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine_ex">SetResourceStatusEx</a> entry point.

### -field SetResourceLockedMode

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_locked_mode_routine">SetResourceLockedMode</a> entry point.

### -field SignalFailure

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-psignal_failure_routine">SignalFailure</a> entry point.

### -field SetResourceInMemoryNodeLocalProperties

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_inmemory_nodelocal_properties_routine">SetResourceInMemoryNodeLocalProperties</a> entry point.

### -field EndControlCall

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pend_control_call">EndControlCall</a> entry point.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.

### -field EndTypeControlCall

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pend_type_control_call">EndTypeControlCall</a> entry point.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.

### -field ExtendControlCall

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pextend_res_control_call">ExtendControlCall</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field ExtendTypeControlCall

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pextend_res_type_control_call">ExtendResTypeControlCall</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field RaiseResTypeNotification

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-praise_res_type_notification">RaiseResTypeNotification</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field ChangeResourceProcessForDumps

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pchange_resource_process_for_dumps">ChangeResourceProcessForDumps</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field ChangeResTypeProcessForDumps

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pchange_res_type_process_for_dumps">ChangeResTypeProcessForDumps</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field SetInternalState

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_internal_state">SetInternalState</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.

### -field SetResourceLockedModeEx

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>