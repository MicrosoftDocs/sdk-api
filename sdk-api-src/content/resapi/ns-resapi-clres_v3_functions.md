---
UID: NS:resapi.CLRES_V3_FUNCTIONS
title: CLRES_V3_FUNCTIONS
author: windows-sdk-content
description: Contains pointers to all Resource API version 3.0 entry points, except StartupEx.
old-location: mscs\clres_v3_functions.htm
old-project: MsCS
ms.assetid: 5D4B5494-5F75-4864-9BA5-EF1A88DFE143
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLRES_V3_FUNCTIONS, CLRES_V3_FUNCTIONS, CLRES_V3_FUNCTIONS structure [Failover Cluster], PCLRES_V3_FUNCTIONS, PCLRES_V3_FUNCTIONS structure pointer [Failover Cluster], mscs.clres_v3_functions, resapi/CLRES_V3_FUNCTIONS, resapi/PCLRES_V3_FUNCTIONS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CLRES_V3_FUNCTIONS, *PCLRES_V3_FUNCTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ResApi.h
api_name:
-	CLRES_V3_FUNCTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CLRES_V3_FUNCTIONS structure


## -description


Contains pointers to all <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> version 3.0 entry 
    points, except <a href="https://msdn.microsoft.com/7C669EDC-B7A1-4623-91A9-5D8C5949B50A">StartupEx</a>.


## -struct-fields




### -field Open

Pointer to the <a href="https://msdn.microsoft.com/EA798D15-9458-4F66-8D0E-13DA383552F7">OpenV2</a> entry point.


### -field Close

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> entry point.


### -field Online

Pointer to the <a href="https://msdn.microsoft.com/0462CDFD-6499-4FF8-8B5C-4DC15AC30169">OnlineV2</a> entry point.


### -field Offline

Pointer to the <a href="https://msdn.microsoft.com/2983B328-08ED-4DA6-8DC2-79D44C710888">OfflineV2</a> entry point.


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


### -field BeginResourceControl

Pointer to the <a href="https://msdn.microsoft.com/1B95607F-658A-469D-8935-DF7E537D1509">BeginResourceControl</a> entry 
      point.


### -field BeginResourceTypeControl

Pointer to the <a href="https://msdn.microsoft.com/9D5D5ADB-9707-4690-9B91-CC99F68DE2A8">BeginResourceTypeControl</a> entry 
      point.


### -field Cancel

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> entry point.


#### - ResourceControl

Not supported starting with Windows Server 2016.

<b>Windows Server 2012 R2:  </b>Pointer to the <a href="https://msdn.microsoft.com/a9c64471-41fa-4101-9a02-ad57add8124c">ResourceControl</a> entry 
      point.


#### - ResourceTypeControl

Not supported starting with Windows Server 2016.

<b>Windows Server 2012 R2:  </b>Pointer to the <a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a> entry 
      point.


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

