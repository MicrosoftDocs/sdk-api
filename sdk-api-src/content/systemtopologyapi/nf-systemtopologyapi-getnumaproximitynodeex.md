---
UID: NF:systemtopologyapi.GetNumaProximityNodeEx
title: GetNumaProximityNodeEx function (systemtopologyapi.h)
description: Retrieves the NUMA node number that corresponds to the specified proximity identifier as a USHORT value.
helpviewer_keywords: ["GetNumaProximityNodeEx","GetNumaProximityNodeEx function","base.getnumaproximitynodeex","systemtopologyapi/GetNumaProximityNodeEx"]
old-location: base\getnumaproximitynodeex.htm
tech.root: ProcThread
ms.assetid: c3da519f-d2bc-4cd0-9c11-587af1ad6e60
ms.date: 12/05/2018
ms.keywords: GetNumaProximityNodeEx, GetNumaProximityNodeEx function, base.getnumaproximitynodeex, systemtopologyapi/GetNumaProximityNodeEx
req.header: systemtopologyapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetNumaProximityNodeEx
 - systemtopologyapi/GetNumaProximityNodeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-systemtopology-l1-1-2.dll
 - kernel32.dll
 - API-MS-Win-Core-Systemtopology-L1-1-1.dll
 - KernelBase.dll
api_name:
 - GetNumaProximityNodeEx
---

# GetNumaProximityNodeEx function


## -description

Retrieves the NUMA node number that corresponds to  the specified proximity identifier as a <b>USHORT</b> value.

## -parameters

### -param ProximityId [in]

The proximity identifier of the node.

### -param NodeNumber [out]

Points to a variable to receive the node number for the specified proximity identifier.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

A proximity domain identifier is an index to a NUMA node on a NUMA system. Proximity domain identifiers are found in the ACPI System Resource Affinity Table (SRAT), where they are used to associate processors and memory regions with a particular NUMA node. Proximity domain identifiers are also found in the ACPI namespace, where they are used to associate a device with a particular NUMA node. Proximity domain identifiers are typically used only by management applications provided by system manufacturers. Windows does not use proximity domain identifiers to identify NUMA nodes; instead, it assigns a unique number to each NUMA node in the system.

The relative distance between nodes on a system is stored in the ACPI System Locality Distance Information Table (SLIT), which is not exposed by any Windows functions. For more information about ACPI tables, see the <a href="https://uefi.org/acpi/specs">ACPI specifications</a>.

The only difference between the <b>GetNumaProximityNodeEx</b> function and the <a href="/windows/desktop/api/winbase/nf-winbase-getnumaproximitynode">GetNumaProximityNode</a> function is the data type of the <i>NodeNumber</i> parameter.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getnumaproximitynode">GetNumaProximityNode</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>