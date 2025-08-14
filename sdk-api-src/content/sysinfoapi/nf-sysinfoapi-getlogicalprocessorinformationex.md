---
UID: NF:sysinfoapi.GetLogicalProcessorInformationEx
title: GetLogicalProcessorInformationEx function (sysinfoapi.h)
description: Retrieves information about the relationships of logical processors and related hardware.
helpviewer_keywords: ["GetLogicalProcessorInformationEx","GetLogicalProcessorInformationEx function","RelationAll","RelationCache","RelationGroup","RelationNumaNode","RelationProcessorCore","RelationProcessorPackage","base.getlogicalprocessorinformationex","sysinfoapi/GetLogicalProcessorInformationEx"]
old-location: base\getlogicalprocessorinformationex.htm
tech.root: backup
ms.assetid: dfc4f444-4651-4a02-b8f6-f30d9278eae2
ms.date: 02/27/2023
ms.keywords: GetLogicalProcessorInformationEx, GetLogicalProcessorInformationEx function, RelationAll, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, RelationProcessorDie, RelationNumaNodeEx, RelationProcessorModule, base.getlogicalprocessorinformationex, sysinfoapi/GetLogicalProcessorInformationEx
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - GetLogicalProcessorInformationEx
 - sysinfoapi/GetLogicalProcessorInformationEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetLogicalProcessorInformationEx
---

# GetLogicalProcessorInformationEx function


## -description

Retrieves information about the relationships of logical processors and related hardware.

## -parameters

### -param RelationshipType [in]

The type of relationship to retrieve. This parameter can be one of the following <a href="/windows/desktop/api/winnt/ne-winnt-logical_processor_relationship">LOGICAL_PROCESSOR_RELATIONSHIP</a> values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<td width="40%"><a id="RelationProcessorCore"></a><a id="relationprocessorcore"></a><a id="RELATIONPROCESSORCORE"></a><dl>
<dt><b>RelationProcessorCore</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a single processor core. 

</td>
</tr>
<tr>
<td width="40%"><a id="RelationNumaNode"></a><a id="relationnumanode"></a><a id="RELATIONNUMANODE"></a><dl>
<dt><b>RelationNumaNode</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that are part of the same NUMA node. 

</td>
</tr>
<tr>
<td width="40%"><a id="RelationCache"></a><a id="relationcache"></a><a id="RELATIONCACHE"></a><dl>
<dt><b>RelationCache</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a cache. 

</td>
</tr>
<tr>
<tr>
<td width="40%"><a id="RelationProcessorPackage"></a><a id="relationprocessorpackage"></a><a id="RELATIONPROCESSORPACKAGE"></a><dl>
<dt><b>RelationProcessorPackage</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a physical package. 

</td>
</tr>
<tr>
<td width="40%"><a id="RelationGroup"></a><a id="relationgroup"></a><a id="RELATIONGROUP"></a><dl>
<dt><b>RelationGroup</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a processor group. 

</td>
</tr>
<tr>
<td width="40%"><a id="RelationProcessorDie"></a><a id="relationprocessordie"></a><a id="RELATIONPROCESSORDIE"></a><dl>
<dt><b>RelationProcessorDie</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a processor die.

</td>
</tr>
</tr>
<td width="40%"><a id="RelationNumaNodeEx"></a><a id="relationnumanodeex"></a><a id="RELATIONNUMANODEEX"></a><dl>
<dt><b>RelationNumaNodeEx</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that are part of the same NUMA node (with full affinity).
</td>
</tr>
<tr>
<td width="40%"><a id="RelationProcessorModule"></a><a id="relationprocessormodule"></a><a id="RELATIONPROCESSORMODULE"></a><dl>
<dt><b>RelationProcessorModule</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors that share a processor module.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationAll"></a><a id="relationall"></a><a id="RELATIONALL"></a><dl>
<dt><b>RelationAll</b></dt>
<dt>0xffff</dt>
</dl>
</td>
<td width="60%">
Retrieves information about logical processors for all relationship types (cache, NUMA node, processor core, physical package, processor group, processor die, and processor module).

</td>
</tr>
</table>

### -param Buffer [out, optional]

A pointer to a buffer that receives a sequence of variable-sized <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structures. If the function fails, the contents of this buffer are undefined.

### -param ReturnedLength [in, out]

On input, specifies the length of the buffer pointed to by  <i>Buffer</i>, in bytes. If the buffer is large enough to contain all of the data, this function succeeds and <i>ReturnedLength</i> is set to the number of bytes returned. If the buffer is not large enough to contain all of the data, the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and <i>ReturnedLength</i> is set to the buffer length required to contain all of the data. If the function fails with an error other than ERROR_INSUFFICIENT_BUFFER, the value of <i>ReturnedLength</i> is undefined.

## -returns

If the function succeeds, the return value is TRUE and at least one <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is written to the output buffer.

If the function fails, the return value is FALSE. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

 If a 32-bit process running under WOW64 calls this function on a system with more than 64 processors, some of the processor affinity masks returned by the function may be incorrect. This is  because the high-order <b>DWORD</b> of the 64-bit <a href="/windows-hardware/drivers/kernel/interrupt-affinity-and-priority">KAFFINITY</a> structure that represents all 64 processors is "folded" into a 32-bit <b>KAFFINITY</b> structure in the caller's buffer. As a result, the affinity masks for processors 32 through 63 are incorrectly represented as duplicates of the masks for processors 0 through 31. In addition, the affinity masks for processors 32 through 63 are incorrectly represented as duplicates of the masks for processors 0 through 31. In addition, the sum of all per-group <b>ActiveProcessorCount</b> and <b>MaximumProcessorCount</b> values reported in <a href="/windows/desktop/api/winnt/ns-winnt-processor_group_info">PROCESSOR_GROUP_INFO</a> structures may exclude some active logical processors.

When this function is called with a relationship type of <b>RelationProcessorCore</b>, it returns a <a href="/windows/desktop/api/winnt/ns-winnt-processor_relationship">PROCESSOR_RELATIONSHIP</a> structure for every active processor core in every processor group in the system. This is by design, because an unaffinitized 32-bit thread can run on any logical processor in a given group, including processors 32 through 63. A 32-bit caller can use the total count of <b>PROCESSOR_RELATIONSHIP</b> structures to determine the actual number of active processor cores on the system. However, the affinity of a 32-bit thread cannot be explicitly set to logical processor 32 through 63 of any processor group.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

### Behavior starting with Windows Server 2022 (21H2, build 20348) ###

The behavior of this and other NUMA functions has been modified to better support systems with nodes containing more that 64 processors. For more information about this change, including information about enabling the old behavior of this API, see [NUMA Support](/windows/win32/procthread/numa-support).

Requests for [RelationNumaNode](../winnt/ne-winnt-logical_processor_relationship.md) will return [NUMA_NODE_RELATIONSHIP](../winnt/ns-winnt-numa_node_relationship.md) structures that contain only the affinity of the node within it's primary group. The [GroupCount](../winnt/ns-winnt-numa_node_relationship.md) value will be 1 and the structure size is fixed.

Requests for **RelationNumaNodeEx** or **RelationAll** will return **NUMA_NODE_RELATIONSHIP** structures that contain an array of affinities for the node over all groups. The **GroupCount** reports the number of affinities and the size of structure is variable.



## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
