---
UID: NS:resapi.CLRES_V3_FUNCTIONS
title: CLRES_V3_FUNCTIONS (resapi.h)
description: Contains pointers to all Resource API version 3.0 entry points, except StartupEx.
helpviewer_keywords: ["*PCLRES_V3_FUNCTIONS","CLRES_V3_FUNCTIONS","CLRES_V3_FUNCTIONS structure [Failover Cluster]","PCLRES_V3_FUNCTIONS","PCLRES_V3_FUNCTIONS structure pointer [Failover Cluster]","mscs.clres_v3_functions","resapi/CLRES_V3_FUNCTIONS","resapi/PCLRES_V3_FUNCTIONS"]
old-location: mscs\clres_v3_functions.htm
tech.root: MsCS
ms.assetid: 5D4B5494-5F75-4864-9BA5-EF1A88DFE143
ms.date: 12/05/2018
ms.keywords: '*PCLRES_V3_FUNCTIONS, CLRES_V3_FUNCTIONS, CLRES_V3_FUNCTIONS structure [Failover Cluster], PCLRES_V3_FUNCTIONS, PCLRES_V3_FUNCTIONS structure pointer [Failover Cluster], mscs.clres_v3_functions, resapi/CLRES_V3_FUNCTIONS, resapi/PCLRES_V3_FUNCTIONS'
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: CLRES_V3_FUNCTIONS, *PCLRES_V3_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLRES_V3_FUNCTIONS
 - resapi/CLRES_V3_FUNCTIONS
 - PCLRES_V3_FUNCTIONS
 - resapi/PCLRES_V3_FUNCTIONS
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
 - CLRES_V3_FUNCTIONS
---

# CLRES_V3_FUNCTIONS structure


## -description

Contains pointers to all <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> version 3.0 entry 
    points, except <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_ex_routine">StartupEx</a>.

## -struct-fields

### -field Open

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_v2_routine">OpenV2</a> entry point.

### -field Close

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a> entry point.

### -field Online

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_v2_routine">OnlineV2</a> entry point.

### -field Offline

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_v2_routine">OfflineV2</a> entry point.

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

### -field BeginResourceControl

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pbegin_rescall_routine">BeginResourceControl</a> entry 
      point.

### -field BeginResourceTypeControl

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pbegin_restypecall_routine">BeginResourceTypeControl</a> entry 
      point.

### -field Cancel

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pcancel_routine">Cancel</a> entry point.


#### - ResourceControl

Not supported starting with Windows Server 2016.

<b>Windows Server 2012 R2:  </b>Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_control_routine">ResourceControl</a> entry 
      point.


#### - ResourceTypeControl

Not supported starting with Windows Server 2016.

<b>Windows Server 2012 R2:  </b>Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a> entry 
      point.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>