---
UID: NS:resapi.CLRES_FUNCTION_TABLE
title: CLRES_FUNCTION_TABLE (resapi.h)
description: Describes a function table for any version of the Resource API.
helpviewer_keywords: ["*PCLRES_FUNCTION_TABLE","CLRES_FUNCTION_TABLE","CLRES_FUNCTION_TABLE structure [Failover Cluster]","CLRES_V1_FUNCTION_SIZE","CLRES_V2_FUNCTION_SIZE","CLRES_V3_FUNCTION_SIZE","CLRES_VERSION_V1_00","CLRES_VERSION_V2_00","CLRES_VERSION_V3_00","PCLRES_FUNCTION_TABLE","PCLRES_FUNCTION_TABLE structure pointer [Failover Cluster]","_wolf_clres_function_table","mscs.clres_function_table","resapi/CLRES_FUNCTION_TABLE","resapi/PCLRES_FUNCTION_TABLE"]
old-location: mscs\clres_function_table.htm
tech.root: MsCS
ms.assetid: fa27076f-393c-415a-9301-91cfe770fb3c
ms.date: 12/05/2018
ms.keywords: '*PCLRES_FUNCTION_TABLE, CLRES_FUNCTION_TABLE, CLRES_FUNCTION_TABLE structure [Failover Cluster], CLRES_V1_FUNCTION_SIZE, CLRES_V2_FUNCTION_SIZE, CLRES_V3_FUNCTION_SIZE, CLRES_VERSION_V1_00, CLRES_VERSION_V2_00, CLRES_VERSION_V3_00, PCLRES_FUNCTION_TABLE, PCLRES_FUNCTION_TABLE structure pointer [Failover Cluster], _wolf_clres_function_table, mscs.clres_function_table, resapi/CLRES_FUNCTION_TABLE, resapi/PCLRES_FUNCTION_TABLE'
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
req.typenames: CLRES_FUNCTION_TABLE, *PCLRES_FUNCTION_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLRES_FUNCTION_TABLE
 - resapi/CLRES_FUNCTION_TABLE
 - PCLRES_FUNCTION_TABLE
 - resapi/PCLRES_FUNCTION_TABLE
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
 - CLRES_FUNCTION_TABLE
---

# CLRES_FUNCTION_TABLE structure


## -description

Describes a function table for any version of the 
    <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a>.

## -struct-fields

### -field TableSize

Count of bytes in the structure.


This can contain one of these values:





#### CLRES_V1_FUNCTION_SIZE

The size of the function table for Resource API version 1.0.



#### CLRES_V2_FUNCTION_SIZE

The size of the function table for Resource API version 2.0.

<b>Windows Server 2008 R2:  </b>This value is not supported before Windows Server 2012.



#### CLRES_V3_FUNCTION_SIZE

The size of the function table for Resource API version 3.0.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.

### -field Version

The supported version of the Resource API.


This can contain one of these values:





#### CLRES_VERSION_V1_00 (0x100)

Resource API version 1.0.



#### CLRES_VERSION_V2_00 (0x200)

Resource API version 2.0.

<b>Windows Server 2008 R2:  </b>This value is not supported before Windows Server 2012.



#### CLRES_VERSION_V3_00 (0x300)

Resource API version 3.0.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.V1Functions

A <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_v1_functions">CLRES_V1_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 1.0.

### -field DUMMYUNIONNAME.V2Functions

A <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_v2_functions">CLRES_V2_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 2.0.

<b>Windows Server 2008 R2:  </b>This member was added in Windows Server 2012.

### -field DUMMYUNIONNAME.V3Functions

A <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_v3_functions">CLRES_V3_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 3.0.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.

### -field DUMMYUNIONNAME.V4Functions

## -remarks

Only the first two members are guaranteed to be at the same offset within the 
     <b>CLRES_FUNCTION_TABLE</b> structure. All other entries 
     within this structure are dependent on the 
     <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> version supported.

The <b>V1Functions</b> member is a 
     <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_v1_functions">CLRES_V1_FUNCTIONS</a> structure containing pointers to 
     all Resource API entry points except <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>. All pointers 
     must be non-<b>NULL</b> except for pointers to the following entry point functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a>
</li>
</ul>
For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-resource-dlls">Implementing Resource DLLs</a>.

To create a function table for version 1.0 of the Resource API, use the 
     <a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clres_v1_function_table">CLRES_V1_FUNCTION_TABLE</a> macro.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/defining-structures-and-constants">Defining Structures and Constants</a> 
      in <a href="/previous-versions/windows/desktop/mscs/implementing-resource-dlls">Implementing Resource DLLs</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>



<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_v1_functions">CLRES_V1_FUNCTIONS</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clres_v1_function_table">CLRES_V1_FUNCTION_TABLE</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_control_routine">ResourceControl</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a>