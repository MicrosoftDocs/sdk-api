---
UID: NS:resapi.CLRES_V4_FUNCTIONS
title: CLRES_V4_FUNCTIONS (resapi.h)
description: Contains pointers to all Resource API version 4.0 entry points, except StartupEx.
helpviewer_keywords: ["*PCLRES_V4_FUNCTIONS","CLRES_V4_FUNCTIONS","CLRES_V4_FUNCTIONS structure [Failover Cluster]","PCLRES_V4_FUNCTIONS","PCLRES_V4_FUNCTIONS structure pointer [Failover Cluster]","mscs.clres_v4_functions","resapi/CLRES_V4_FUNCTIONS","resapi/PCLRES_V4_FUNCTIONS"]
old-location: mscs\clres_v4_functions.htm
tech.root: MsCS
ms.assetid: B3722540-2AC2-4B31-A22B-D40DE0AFA7BD
ms.date: 12/05/2018
ms.keywords: '*PCLRES_V4_FUNCTIONS, CLRES_V4_FUNCTIONS, CLRES_V4_FUNCTIONS structure [Failover Cluster], PCLRES_V4_FUNCTIONS, PCLRES_V4_FUNCTIONS structure pointer [Failover Cluster], mscs.clres_v4_functions, resapi/CLRES_V4_FUNCTIONS, resapi/PCLRES_V4_FUNCTIONS'
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
req.typenames: CLRES_V4_FUNCTIONS, *PCLRES_V4_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLRES_V4_FUNCTIONS
 - resapi/CLRES_V4_FUNCTIONS
 - PCLRES_V4_FUNCTIONS
 - resapi/PCLRES_V4_FUNCTIONS
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
 - CLRES_V4_FUNCTIONS
---

# CLRES_V4_FUNCTIONS structure


## -description

Contains pointers to all <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> version 4.0 entry 
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

### -field BeginResourceControlAsUser

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pbegin_rescall_as_user_routine">BeginResourceControlAsUser</a> entry point.

### -field BeginResourceTypeControlAsUser

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pbegin_restypecall_as_user_routine">BeginResourceTypeControlAsUser</a> entry point.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>