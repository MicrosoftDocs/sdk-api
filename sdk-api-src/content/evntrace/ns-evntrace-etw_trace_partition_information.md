---
UID: NS:evntrace._ETW_TRACE_PARTITION_INFORMATION
title: ETW_TRACE_PARTITION_INFORMATION (evntrace.h)
description: Contains partition information pulled from an ETW trace.helpviewer_keywords: ["*PETW_TRACE_PARTITION_INFORMATION","ETW_TRACE_PARTITION_INFORMATION","ETW_TRACE_PARTITION_INFORMATION structure [ETW]","PETW_TRACE_PARTITION_INFORMATION","PETW_TRACE_PARTITION_INFORMATION structure pointer [ETW]","Process","VmDirectUvm","VmHost","VmHostedUvm","_ETW_TRACE_PARTITION_INFORMATION","etw.etw_trace_partition_information","evntrace/ETW_TRACE_PARTITION_INFORMATION","evntrace/PETW_TRACE_PARTITION_INFORMATION"]
old-location: etw\etw_trace_partition_information.htm
tech.root: ETW
ms.assetid: 8D8F8E79-B273-417A-B8C2-6CE4FC454C07
ms.date: 12/05/2018
ms.keywords: '*PETW_TRACE_PARTITION_INFORMATION, ETW_TRACE_PARTITION_INFORMATION, ETW_TRACE_PARTITION_INFORMATION structure [ETW], PETW_TRACE_PARTITION_INFORMATION, PETW_TRACE_PARTITION_INFORMATION structure pointer [ETW], Process, VmDirectUvm, VmHost, VmHostedUvm, _ETW_TRACE_PARTITION_INFORMATION, etw.etw_trace_partition_information, evntrace/ETW_TRACE_PARTITION_INFORMATION, evntrace/PETW_TRACE_PARTITION_INFORMATION'
f1_keywords:
- evntrace/ETW_TRACE_PARTITION_INFORMATION
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- evntrace.h
api_name:
- ETW_TRACE_PARTITION_INFORMATION
targetos: Windows
req.typenames: ETW_TRACE_PARTITION_INFORMATION, *PETW_TRACE_PARTITION_INFORMATION
req.redist: 
ms.custom: 19H1
---

# ETW_TRACE_PARTITION_INFORMATION structure


## -description


Contains partition information pulled from an ETW trace. Most commonly used as a return structure for <a href="https://docs.microsoft.com/windows/desktop/ETW/querytraceprocessinghandle">QueryTraceProcessingHandle</a>.


## -struct-fields




### -field PartitionId

GUID to identify the machine. 




### -field ParentId

GUID that identifies the partition instance that contains the traced partition.  If the traced partition is a host, then <b>ParentId</b> will be 0.


### -field QpcOffsetFromRoot

 


### -field PartitionType

Enumeration value of the container type. the value may be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Process"></a><a id="process"></a><a id="PROCESS"></a><dl>
<dt><b>Process</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
For events originating from inside a “Windows Server Container”.

</td>
</tr>
<tr>
<td width="40%"><a id="VmHost"></a><a id="vmhost"></a><a id="VMHOST"></a><dl>
<dt><b>VmHost</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
For events originating from inside a “Hyper-V Container”.

</td>
</tr>
<tr>
<td width="40%"><a id="VmHostedUvm"></a><a id="vmhosteduvm"></a><a id="VMHOSTEDUVM"></a><dl>
<dt><b>VmHostedUvm</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
For events originating from a “Hyper-V Container” template virtual machine.

</td>
</tr>
<tr>
<td width="40%"><a id="VmDirectUvm"></a><a id="vmdirectuvm"></a><a id="VMDIRECTUVM"></a><dl>
<dt><b>VmDirectUvm</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
For events originating from applications running with  <a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows Defender Application Guard</a>.

</td>
</tr>
</table>
 


#### - Reserved

Reserved for future use.

