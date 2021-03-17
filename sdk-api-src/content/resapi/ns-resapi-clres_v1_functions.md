---
UID: NS:resapi.CLRES_V1_FUNCTIONS
title: CLRES_V1_FUNCTIONS (resapi.h)
description: Contains pointers to all Resource API version 1.0 entry points except Startup.
helpviewer_keywords: ["*PCLRES_V1_FUNCTIONS","CLRES_V1_FUNCTIONS","CLRES_V1_FUNCTIONS structure [Failover Cluster]","PCLRES_V1_FUNCTIONS","PCLRES_V1_FUNCTIONS structure pointer [Failover Cluster]","_wolf_clres_v1_functions","mscs.clres_v1_functions","resapi/CLRES_V1_FUNCTIONS","resapi/PCLRES_V1_FUNCTIONS"]
old-location: mscs\clres_v1_functions.htm
tech.root: MsCS
ms.assetid: 54299e92-8b9d-4611-8147-8e7a5e1c8e34
ms.date: 12/05/2018
ms.keywords: '*PCLRES_V1_FUNCTIONS, CLRES_V1_FUNCTIONS, CLRES_V1_FUNCTIONS structure [Failover Cluster], PCLRES_V1_FUNCTIONS, PCLRES_V1_FUNCTIONS structure pointer [Failover Cluster], _wolf_clres_v1_functions, mscs.clres_v1_functions, resapi/CLRES_V1_FUNCTIONS, resapi/PCLRES_V1_FUNCTIONS'
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
req.typenames: CLRES_V1_FUNCTIONS, *PCLRES_V1_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLRES_V1_FUNCTIONS
 - resapi/CLRES_V1_FUNCTIONS
 - PCLRES_V1_FUNCTIONS
 - resapi/PCLRES_V1_FUNCTIONS
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
 - CLRES_V1_FUNCTIONS
---

# CLRES_V1_FUNCTIONS structure


## -description

Contains pointers to all <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> version 1.0 entry 
    points except <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>.

## -struct-fields

### -field Open

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point.

### -field Close

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a> entry point.

### -field Online

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> entry point.

### -field Offline

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> entry point.

### -field Terminate

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> entry point.

### -field LooksAlive

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a> entry point.

### -field IsAlive

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a> entry point.

### -field Arbitrate

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a> entry point.

### -field Release

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a> entry point.

### -field ResourceControl

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_control_routine">ResourceControl</a> entry 
      point.

### -field ResourceTypeControl

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a> entry 
      point.

## -remarks

The <b>CLRES_V1_FUNCTIONS</b> structure is the function 
    table that is returned by the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a> function in 
    <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> 1.0. 
    <a href="/previous-versions/windows/desktop/mscs/resource-dlls">Resource DLLs</a> that support multiple 
    <a href="/previous-versions/windows/desktop/mscs/resource-types">resource types</a> must provide one function table for each 
    resource type. All function pointers must be non-NULL except for the following entry points:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_control_routine">ResourceControl</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a>
</li>
</ul>
For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/implementing-resource-dlls">Implementing Resource DLLs</a>.

To create a function table for version 1.0 of the Resource API, use the 
    <a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clres_v1_function_table">CLRES_V1_FUNCTION_TABLE</a> macro.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clres_v1_function_table">CLRES_V1_FUNCTION_TABLE</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a>



<b>ResourceControl</b>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>