---
UID: NF:winbase.GetNumaProximityNode
title: GetNumaProximityNode function (winbase.h)
description: Retrieves the NUMA node number that corresponds to the specified proximity domain identifier.
helpviewer_keywords: ["GetNumaProximityNode","GetNumaProximityNode function","base.getnumaproximitynode","winbase/GetNumaProximityNode"]
old-location: base\getnumaproximitynode.htm
tech.root: backup
ms.assetid: 9a2dbfe3-13e7-442d-a5f6-b2632878f618
ms.date: 12/05/2018
ms.keywords: GetNumaProximityNode, GetNumaProximityNode function, base.getnumaproximitynode, winbase/GetNumaProximityNode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNumaProximityNode
 - winbase/GetNumaProximityNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetNumaProximityNode
---

# GetNumaProximityNode function


## -description

Retrieves the NUMA node number that corresponds to the specified proximity domain identifier.

Use the <a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex">GetNumaProximityNodeEx</a> function to retrieve the node number as a <b>USHORT</b> value.

## -parameters

### -param ProximityId [in]

The proximity domain identifier of the node.

### -param NodeNumber [out]

The node number. If the processor does not exist, this parameter is 0xFF.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error  information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A proximity domain identifier is an index to a NUMA node on a NUMA system. Proximity domain identifiers are found in the ACPI System Resource Affinity Table (SRAT), where they are used to associate processors and memory regions with a particular NUMA node. Proximity domain identifiers are also found in the ACPI namespace, where they are used to associate a device with a particular NUMA node. Proximity domain identifiers are typically used only by management applications provided by system manufacturers. Windows does not use proximity domain identifiers to identify NUMA nodes; instead, it assigns a unique number to each NUMA node in the system.

The relative distance between nodes on a system is stored in the ACPI System Locality Distance Information Table (SLIT), which is not exposed by any Windows functions. For more information about ACPI tables, see the <a href="https://uefi.org/acpi/specs">ACPI specifications</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumaprocessornode">GetNumaProcessorNode</a>



<a href="/windows/desktop/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex">GetNumaProximityNodeEx</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>