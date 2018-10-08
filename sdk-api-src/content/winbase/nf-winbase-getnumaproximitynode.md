---
UID: NF:winbase.GetNumaProximityNode
title: GetNumaProximityNode function
author: windows-sdk-content
description: Retrieves the NUMA node number that corresponds to the specified proximity domain identifier.
old-location: base\getnumaproximitynode.htm
tech.root: procthread
ms.assetid: 9a2dbfe3-13e7-442d-a5f6-b2632878f618
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetNumaProximityNode, GetNumaProximityNode function, base.getnumaproximitynode, winbase/GetNumaProximityNode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetNumaProximityNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumaProximityNode function


## -description


Retrieves the NUMA node number that corresponds to the specified proximity domain identifier.

Use the <a href="https://msdn.microsoft.com/c3da519f-d2bc-4cd0-9c11-587af1ad6e60">GetNumaProximityNodeEx</a> function to retrieve the node number as a <b>USHORT</b> value.


## -parameters




### -param ProximityId [in]

The proximity domain identifier of the node.


### -param NodeNumber [out]

The node number. If the processor does not exist, this parameter is 0xFF.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error  information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A proximity domain identifier is an index to a NUMA node on a NUMA system. Proximity domain identifiers are found in the ACPI System Resource Affinity Table (SRAT), where they are used to associate processors and memory regions with a particular NUMA node. Proximity domain identifiers are also found in the ACPI namespace, where they are used to associate a device with a particular NUMA node. Proximity domain identifiers are typically used only by management applications provided by system manufacturers. Windows does not use proximity domain identifiers to identify NUMA nodes; instead, it assigns a unique number to each NUMA node in the system.

The relative distance between nodes on a system is stored in the ACPI System Locality Distance Information Table (SLIT), which is not exposed by any Windows functions. For more information about ACPI tables, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=84013">ACPI specifications</a>. 




## -see-also




<a href="https://msdn.microsoft.com/88e6c6b3-7ec5-43e5-8cf3-21402925f718">GetNumaProcessorNode</a>



<a href="https://msdn.microsoft.com/c3da519f-d2bc-4cd0-9c11-587af1ad6e60">GetNumaProximityNodeEx</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>
 

 

