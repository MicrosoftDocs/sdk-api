---
UID: NS:resapi.CLRES_FUNCTION_TABLE
title: CLRES_FUNCTION_TABLE
author: windows-sdk-content
description: Describes a function table for any version of the Resource API.
old-location: mscs\clres_function_table.htm
old-project: MsCS
ms.assetid: fa27076f-393c-415a-9301-91cfe770fb3c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLRES_FUNCTION_TABLE, CLRES_FUNCTION_TABLE, CLRES_FUNCTION_TABLE structure [Failover Cluster], CLRES_V1_FUNCTION_SIZE, CLRES_V2_FUNCTION_SIZE, CLRES_V3_FUNCTION_SIZE, CLRES_VERSION_V1_00, CLRES_VERSION_V2_00, CLRES_VERSION_V3_00, PCLRES_FUNCTION_TABLE, PCLRES_FUNCTION_TABLE structure pointer [Failover Cluster], _wolf_clres_function_table, mscs.clres_function_table, resapi/CLRES_FUNCTION_TABLE, resapi/PCLRES_FUNCTION_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: CLRES_FUNCTION_TABLE, *PCLRES_FUNCTION_TABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ResApi.h
api_name:
-	CLRES_FUNCTION_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CLRES_FUNCTION_TABLE structure


## -description


Describes a function table for any version of the 
    <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a>.


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

A <a href="https://msdn.microsoft.com/54299e92-8b9d-4611-8147-8e7a5e1c8e34">CLRES_V1_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 1.0.


### -field DUMMYUNIONNAME.V2Functions

A <a href="https://msdn.microsoft.com/81A5169E-C2AB-4666-9D9F-9DE4A639D0D6">CLRES_V2_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 2.0.

<b>Windows Server 2008 R2:  </b>This member was added in Windows Server 2012.


### -field DUMMYUNIONNAME.V3Functions

A <a href="https://msdn.microsoft.com/5D4B5494-5F75-4864-9BA5-EF1A88DFE143">CLRES_V3_FUNCTIONS</a> structure that contains the 
        table of entry points included in the Resource API version 3.0.

<b>Windows Server 2008 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.


### -field DUMMYUNIONNAME.V4Functions

 




## -remarks



Only the first two members are guaranteed to be at the same offset within the 
     <b>CLRES_FUNCTION_TABLE</b> structure. All other entries 
     within this structure are dependent on the 
     <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> version supported.

The <b>V1Functions</b> member is a 
     <a href="https://msdn.microsoft.com/54299e92-8b9d-4611-8147-8e7a5e1c8e34">CLRES_V1_FUNCTIONS</a> structure containing pointers to 
     all Resource API entry points except <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a>. All pointers 
     must be non-<b>NULL</b> except for pointers to the following entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9e8e4557-b223-4f8f-9393-67f589181754">Release</a>
</li>
</ul>
For more information, see 
     <a href="https://msdn.microsoft.com/400862c3-73c4-443d-bc60-1c1b6b34534f">Implementing Resource DLLs</a>.

To create a function table for version 1.0 of the Resource API, use the 
     <a href="https://msdn.microsoft.com/2c390cbb-3bff-4850-9496-8991c112c233">CLRES_V1_FUNCTION_TABLE</a> macro.


#### Examples

See <a href="https://msdn.microsoft.com/20b150b4-293f-408b-888e-bac2b2fa4fb8">Defining Structures and Constants</a> 
      in <a href="https://msdn.microsoft.com/400862c3-73c4-443d-bc60-1c1b6b34534f">Implementing Resource DLLs</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>



<a href="https://msdn.microsoft.com/54299e92-8b9d-4611-8147-8e7a5e1c8e34">CLRES_V1_FUNCTIONS</a>



<a href="https://msdn.microsoft.com/2c390cbb-3bff-4850-9496-8991c112c233">CLRES_V1_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/9e8e4557-b223-4f8f-9393-67f589181754">Release</a>



<a href="https://msdn.microsoft.com/a9c64471-41fa-4101-9a02-ad57add8124c">ResourceControl</a>



<a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a>
 

 

