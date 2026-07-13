---
UID: NS:evntrace._ETW_TRACE_PARTITION_INFORMATION
title: ETW_TRACE_PARTITION_INFORMATION (evntrace.h)
description: Contains partition information pulled from an ETW trace.
helpviewer_keywords:
  [
    "*PETW_TRACE_PARTITION_INFORMATION",
    "ETW_TRACE_PARTITION_INFORMATION",
    "ETW_TRACE_PARTITION_INFORMATION structure [ETW]",
    "PETW_TRACE_PARTITION_INFORMATION",
    "PETW_TRACE_PARTITION_INFORMATION structure pointer [ETW]",
    "Process",
    "VmDirectUvm",
    "VmHost",
    "VmHostedUvm",
    "_ETW_TRACE_PARTITION_INFORMATION",
    "etw.etw_trace_partition_information",
    "evntrace/ETW_TRACE_PARTITION_INFORMATION",
    "evntrace/PETW_TRACE_PARTITION_INFORMATION",
  ]
old-location: etw\etw_trace_partition_information.htm
tech.root: ETW
ms.assetid: 8D8F8E79-B273-417A-B8C2-6CE4FC454C07
ms.date: 12/05/2018
ms.keywords:
  "*PETW_TRACE_PARTITION_INFORMATION, ETW_TRACE_PARTITION_INFORMATION,
  ETW_TRACE_PARTITION_INFORMATION structure [ETW],
  PETW_TRACE_PARTITION_INFORMATION, PETW_TRACE_PARTITION_INFORMATION structure
  pointer [ETW], Process, VmDirectUvm, VmHost, VmHostedUvm,
  _ETW_TRACE_PARTITION_INFORMATION, etw.etw_trace_partition_information,
  evntrace/ETW_TRACE_PARTITION_INFORMATION,
  evntrace/PETW_TRACE_PARTITION_INFORMATION"
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
targetos: Windows
req.typenames:
  ETW_TRACE_PARTITION_INFORMATION, *PETW_TRACE_PARTITION_INFORMATION
req.redist:
ms.custom: 19H1
f1_keywords:
  - _ETW_TRACE_PARTITION_INFORMATION
  - evntrace/_ETW_TRACE_PARTITION_INFORMATION
  - PETW_TRACE_PARTITION_INFORMATION
  - evntrace/PETW_TRACE_PARTITION_INFORMATION
  - ETW_TRACE_PARTITION_INFORMATION
  - evntrace/ETW_TRACE_PARTITION_INFORMATION
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - evntrace.h
api_name:
  - ETW_TRACE_PARTITION_INFORMATION
---

## -description

Contains partition information pulled from an ETW trace. Most commonly used as a
return structure for
[QueryTraceProcessingHandle](/windows/win32/api/evntrace/nf-evntrace-querytraceprocessinghandle).

## -struct-fields

### -field PartitionId

GUID to identify the machine.

### -field ParentId

GUID that identifies the partition instance that contains the traced partition.
If the traced partition is a host, then **ParentId** will be 0.

### -field QpcOffsetFromRoot

Reserved for future use.

### -field PartitionType

Enumeration value of the container type. the value may be one of the following:

- **Process** (1): For events originating from inside a "Windows Server
  Container".

- **VmHost** (2): For events originating from inside a "Hyper-V Container".

- **VmHostedUvm** (3): For events originating from a "Hyper-V Container"
  template virtual machine.

- **VmDirectUvm** (4): For events originating from applications running with
  [Microsoft Defender Application Guard (MDAG)](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).
