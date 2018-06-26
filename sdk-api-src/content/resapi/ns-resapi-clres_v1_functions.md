---
UID: NS:resapi.CLRES_V1_FUNCTIONS
title: CLRES_V1_FUNCTIONS
author: windows-sdk-content
description: Contains pointers to all Resource API version 1.0 entry points except Startup.
old-location: mscs\clres_v1_functions.htm
old-project: MsCS
ms.assetid: 54299e92-8b9d-4611-8147-8e7a5e1c8e34
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PCLRES_V1_FUNCTIONS, CLRES_V1_FUNCTIONS, CLRES_V1_FUNCTIONS structure [Failover Cluster], PCLRES_V1_FUNCTIONS, PCLRES_V1_FUNCTIONS structure pointer [Failover Cluster], _wolf_clres_v1_functions, mscs.clres_v1_functions, resapi/CLRES_V1_FUNCTIONS, resapi/PCLRES_V1_FUNCTIONS"
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
tech.root: 
req.typenames: CLRES_V1_FUNCTIONS, *PCLRES_V1_FUNCTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLRES_V1_FUNCTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# CLRES_V1_FUNCTIONS structure


## -description


Contains pointers to all <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> version 1.0 entry 
    points except <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a>.


## -struct-fields




### -field Open

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> entry point.


### -field Close

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> entry point.


### -field Online

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> entry point.


### -field Offline

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> entry point.


### -field Terminate

Pointer to the <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> entry point.


### -field LooksAlive

Pointer to the <a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a> entry point.


### -field IsAlive

Pointer to the <a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a> entry point.


### -field Arbitrate

Pointer to the <a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a> entry point.


### -field Release

Pointer to the <a href="https://msdn.microsoft.com/9e8e4557-b223-4f8f-9393-67f589181754">Release</a> entry point.


### -field ResourceControl

Pointer to the <a href="https://msdn.microsoft.com/a9c64471-41fa-4101-9a02-ad57add8124c">ResourceControl</a> entry 
      point.


### -field ResourceTypeControl

Pointer to the <a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a> entry 
      point.


## -remarks



The <b>CLRES_V1_FUNCTIONS</b> structure is the function 
    table that is returned by the <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a> function in 
    <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> 1.0. 
    <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">Resource DLLs</a> that support multiple 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> must provide one function table for each 
    resource type. All function pointers must be non-NULL except for the following entry points:

<ul>
<li>
<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9e8e4557-b223-4f8f-9393-67f589181754">Release</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9c64471-41fa-4101-9a02-ad57add8124c">ResourceControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a>
</li>
</ul>
For more information, see 
    <a href="https://msdn.microsoft.com/400862c3-73c4-443d-bc60-1c1b6b34534f">Implementing Resource DLLs</a>.

To create a function table for version 1.0 of the Resource API, use the 
    <a href="https://msdn.microsoft.com/2c390cbb-3bff-4850-9496-8991c112c233">CLRES_V1_FUNCTION_TABLE</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>



<a href="https://msdn.microsoft.com/2c390cbb-3bff-4850-9496-8991c112c233">CLRES_V1_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>



<a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a>



<a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<a href="https://msdn.microsoft.com/9e8e4557-b223-4f8f-9393-67f589181754">Release</a>



<b>ResourceControl</b>



<a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a>



<a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a>



<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
 

 

