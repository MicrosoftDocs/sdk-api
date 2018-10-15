---
UID: NS:resapi.CLRES_V4_FUNCTIONS
title: CLRES_V4_FUNCTIONS
author: windows-sdk-content
description: Contains pointers to all Resource API version 4.0 entry points, except StartupEx.
old-location: mscs\clres_v4_functions.htm
tech.root: mscs
ms.assetid: B3722540-2AC2-4B31-A22B-D40DE0AFA7BD
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PCLRES_V4_FUNCTIONS, CLRES_V4_FUNCTIONS, CLRES_V4_FUNCTIONS structure [Failover Cluster], PCLRES_V4_FUNCTIONS, PCLRES_V4_FUNCTIONS structure pointer [Failover Cluster], mscs.clres_v4_functions, resapi/CLRES_V4_FUNCTIONS, resapi/PCLRES_V4_FUNCTIONS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLRES_V4_FUNCTIONS
product: Windows
targetos: Windows
req.typenames: CLRES_V4_FUNCTIONS, *PCLRES_V4_FUNCTIONS
req.redist: 
---

# CLRES_V4_FUNCTIONS structure


## -description


Contains pointers to all <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> version 4.0 entry 
    points, except <a href="https://msdn.microsoft.com/7C669EDC-B7A1-4623-91A9-5D8C5949B50A">StartupEx</a>.


## -struct-fields




### -field Open

Pointer to the <a href="https://msdn.microsoft.com/EA798D15-9458-4F66-8D0E-13DA383552F7">OpenV2</a> entry point.


### -field Close

Pointer to the <a href="https://msdn.microsoft.com/c7c74440-c98a-4440-8bf4-10ebd1a68608">Close</a> entry point.


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

Pointer to the <a href="https://msdn.microsoft.com/F2A22C00-5B25-48F7-BB25-9C351A47B770">Cancel</a> entry point.


### -field BeginResourceControlAsUser

Pointer to the <a href="https://msdn.microsoft.com/58F065C6-0AE1-481D-ADA0-CF2907CB45DC">BeginResourceControlAsUser</a> entry point.


### -field BeginResourceTypeControlAsUser

Pointer to the <a href="https://msdn.microsoft.com/0A95F509-0B07-4E6C-B200-FCF11A0A95F0">BeginResourceTypeControlAsUser</a> entry point.


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

