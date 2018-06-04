---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PSS_QUERY_INFORMATION_CLASS enumeration


## -description


Specifies what information <a href="https://msdn.microsoft.com/D9580147-28ED-4FF5-B7DB-844ACB19769F">PssQuerySnapshot</a> function returns.


## -enum-fields




### -field PSS_QUERY_PROCESS_INFORMATION

Returns a <a href="https://msdn.microsoft.com/D629FA42-B501-4A0E-9B53-6D70E580B687">PSS_PROCESS_INFORMATION</a> structure, with information about the original process.


### -field PSS_QUERY_VA_CLONE_INFORMATION

Returns a <a href="https://msdn.microsoft.com/F93D61B0-EDB2-4560-A69F-CF839EC98B53">PSS_VA_CLONE_INFORMATION</a> structure, with a handle to the VA clone.


### -field PSS_QUERY_AUXILIARY_PAGES_INFORMATION

Returns a <a href="https://msdn.microsoft.com/122DD3DF-002A-4250-9E37-BA239638A684">PSS_AUXILIARY_PAGES_INFORMATION</a> structure, which contains the count of auxiliary pages captured.


### -field PSS_QUERY_VA_SPACE_INFORMATION

Returns a <a href="https://msdn.microsoft.com/F38FF7EB-DDC5-4692-8F57-8D633193D891">PSS_VA_SPACE_INFORMATION</a> structure, which contains the count of regions captured.


### -field PSS_QUERY_HANDLE_INFORMATION

Returns a <a href="https://msdn.microsoft.com/77192849-D919-4947-9BFF-343C166C5A51">PSS_HANDLE_INFORMATION</a> structure, which contains the count of handles captured.


### -field PSS_QUERY_THREAD_INFORMATION

Returns a <a href="https://msdn.microsoft.com/68BC42FD-9A30-462F-AFB1-DF9587C50F45">PSS_THREAD_INFORMATION</a> structure, which contains the count of threads captured.


### -field PSS_QUERY_HANDLE_TRACE_INFORMATION

Returns a <a href="https://msdn.microsoft.com/0877DF1F-044C-48F2-9BCC-938EBD6D46EE">PSS_HANDLE_TRACE_INFORMATION</a> structure, which contains a handle to the handle trace section, and its size.


### -field PSS_QUERY_PERFORMANCE_COUNTERS

Returns a <a href="https://msdn.microsoft.com/298C1FC8-D19D-4DB3-84AA-3870D06B16A1">PSS_PERFORMANCE_COUNTERS</a> structure, which contains various performance counters.


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

