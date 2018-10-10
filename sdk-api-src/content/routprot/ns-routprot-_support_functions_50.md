---
UID: NS:routprot._SUPPORT_FUNCTIONS_50
title: "_SUPPORT_FUNCTIONS_50"
author: windows-sdk-content
description: The SUPPORT_FUNCTIONS structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.
old-location: rras\support_functions.htm
tech.root: Benchmark
ms.assetid: c6e1e3a3-2c2a-40ef-965f-554263614bdf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS, PSUPPORT_FUNCTIONS structure pointer [RAS], SUPPORT_FUNCTIONS, SUPPORT_FUNCTIONS structure [RAS], SUPPORT_FUNCTIONS_50, _SUPPORT_FUNCTIONS_50, _mpr_support_functions, routprot/PSUPPORT_FUNCTIONS, routprot/SUPPORT_FUNCTIONS, rras.support_functions"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Routprot.h
api_name:
 - SUPPORT_FUNCTIONS
product: Windows
targetos: Windows
req.typenames: SUPPORT_FUNCTIONS_50
req.redist: 
---

# _SUPPORT_FUNCTIONS_50 structure


## -description


The 
<b>SUPPORT_FUNCTIONS</b> structure is used by the router manager to pass the routing protocol a set of pointers to functions provided by the router manager.


## -struct-fields




### -field _Align8


### -field dwVersion


### -field dwReserved


#### - DemandDialRequest

Pointer to the 
<a href="https://msdn.microsoft.com/2951d4d2-fdf5-47ed-b9bc-8268b95b8a6e">DemandDialRequest</a> function provided by the router manager for the routing protocol.


#### - MIBEntryCreate

Pointer to the 
<a href="https://msdn.microsoft.com/a65731ec-483d-4e50-aac2-5d55fdac3e3a">MIBEntryCreate</a> function provided by the router manager for the routing protocol.


#### - MIBEntryDelete

Pointer to the 
<a href="https://msdn.microsoft.com/9108ece9-ecac-44cc-b8cb-79a8381e698b">MIBEntryDelete</a> function provided by the router manager for the routing protocol.


#### - MIBEntryGet

Pointer to the 
<a href="https://msdn.microsoft.com/b6807048-5898-4b61-bccf-2644ecdbbda6">MIBEntryGet</a> function provided by the router manager for the routing protocol.


#### - MIBEntryGetFirst

Pointer to the 
<a href="https://msdn.microsoft.com/faa7222b-a862-4395-87e7-203055b34165">MIBEntryGetFirst</a> function provided by the router manager for the routing protocol.


#### - MIBEntryGetNext

Pointer to the 
<a href="https://msdn.microsoft.com/7332e966-06da-4a25-b57c-6dcc851db98a">MIBEntryGetNext</a> function provided by the router manager for the routing protocol.


#### - MIBEntrySet

Pointer to the 
<a href="https://msdn.microsoft.com/f80d0bda-9e03-40ee-8ec5-45c806091d3d">MIBEntrySet</a> function provided by the router manager for the routing protocol.


#### - SetInterfaceReceiveType

Pointer to the 
<a href="https://msdn.microsoft.com/3d350f63-13d6-4ed3-b0be-215b91658e0a">SetInterfaceReceiveType</a> function provided by the router manager for the routing protocol.


#### - ValidateRoute

Pointer to the 
<a href="https://msdn.microsoft.com/f70bd4bb-8d3c-4408-9e83-4482c5ef8d70">ValidateRoute</a> function provided by the router manager for the routing protocol.


## -see-also




<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a>
 

 

