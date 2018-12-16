---
UID: NS:evntrace._ETW_TRACE_PARTITION_INFORMATION
title: ETW_TRACE_PARTITION_INFORMATION
author: windows-sdk-content
description: Contains partition information pulled from an ETW trace.
old-location: etw\etw_trace_partition_information.htm
tech.root: etw
ms.assetid: 8D8F8E79-B273-417A-B8C2-6CE4FC454C07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PETW_TRACE_PARTITION_INFORMATION, ETW_TRACE_PARTITION_INFORMATION, ETW_TRACE_PARTITION_INFORMATION structure [ETW], PETW_TRACE_PARTITION_INFORMATION, PETW_TRACE_PARTITION_INFORMATION structure pointer [ETW], Process, VmDirectUvm, VmHost, VmHostedUvm, _ETW_TRACE_PARTITION_INFORMATION, etw.etw_trace_partition_information, evntrace/ETW_TRACE_PARTITION_INFORMATION, evntrace/PETW_TRACE_PARTITION_INFORMATION"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: ETW_TRACE_PARTITION_INFORMATION, *PETW_TRACE_PARTITION_INFORMATION
req.redist: 
---

# ETW_TRACE_PARTITION_INFORMATION structure


## -description


Contains partition information pulled from an ETW trace. Most commonly used as a return structure for <a href="https://msdn.microsoft.com/87666275-8752-4EC8-9C01-16D36AE4C5E8">QueryTraceProcessingHandle</a>.


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
For events originating from applications running with  <a href="https://blogs.windows.com/msedgedev/2016/09/27/application-guard-microsoft-edge/">Windows Defender Application Guard</a>.

</td>
</tr>
</table>
 


#### - Reserved

Reserved for future use.

