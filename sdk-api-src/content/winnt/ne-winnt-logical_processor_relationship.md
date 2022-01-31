---
UID: NE:winnt._LOGICAL_PROCESSOR_RELATIONSHIP
title: LOGICAL_PROCESSOR_RELATIONSHIP (winnt.h)
description: Represents the relationship between the processor set identified in the corresponding SYSTEM_LOGICAL_PROCESSOR_INFORMATION or SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure.
helpviewer_keywords: ["LOGICAL_PROCESSOR_RELATIONSHIP","LOGICAL_PROCESSOR_RELATIONSHIP enumeration","RelationAll","RelationCache","RelationGroup","RelationNumaNode","RelationProcessorCore","RelationProcessorPackage","base.logical_processor_relationship","winnt/LOGICAL_PROCESSOR_RELATIONSHIP","winnt/RelationAll","winnt/RelationCache","winnt/RelationGroup","winnt/RelationNumaNode","winnt/RelationProcessorCore","winnt/RelationProcessorPackage"]
old-location: base\logical_processor_relationship.htm
tech.root: backup
ms.assetid: 2ada52f0-70ec-4146-9ef7-9af3b08996f9
ms.date: 12/05/2018
ms.keywords: LOGICAL_PROCESSOR_RELATIONSHIP, LOGICAL_PROCESSOR_RELATIONSHIP enumeration, RelationAll, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, base.logical_processor_relationship, winnt/LOGICAL_PROCESSOR_RELATIONSHIP, winnt/RelationAll, winnt/RelationCache, winnt/RelationGroup, winnt/RelationNumaNode, winnt/RelationProcessorCore, winnt/RelationProcessorPackage
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: LOGICAL_PROCESSOR_RELATIONSHIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOGICAL_PROCESSOR_RELATIONSHIP
 - winnt/_LOGICAL_PROCESSOR_RELATIONSHIP
 - LOGICAL_PROCESSOR_RELATIONSHIP
 - winnt/LOGICAL_PROCESSOR_RELATIONSHIP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - LOGICAL_PROCESSOR_RELATIONSHIP
---

# LOGICAL_PROCESSOR_RELATIONSHIP enumeration


## -description

Represents the relationship between the processor set identified in the corresponding [SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX](./ns-winnt-system_logical_processor_information_ex.md)  structure.

## -enum-fields

### -field RelationProcessorCore

The specified logical processors share a single processor core.

### -field RelationNumaNode

The specified logical processors  are part of the same NUMA node.

### -field RelationCache

The specified logical processors  share a cache. 

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.

### -field RelationProcessorPackage

The specified logical processors share a physical package (a single package socketed or soldered onto a motherboard may contain multiple processor cores or threads, each of which is treated as a separate processor by the operating system).

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.

### -field RelationGroup

The specified logical processors share a single <a href="/windows/desktop/ProcThread/processor-groups">processor group</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This value is not supported until Windows Server 2008 R2.

### -field RelationNumaNodeEx

Introduced in TBD - Release Iron.  Requests that the full affinity be returned. Unlike the other relation types, **RelationNumaNodeEx** is not used on input. It is simply a request for **RelationNumaNode** with full group information.

### -field RelationAll:0xffff

On input, retrieves information about all possible relationship types. This value is not used on output.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This value is not supported  until Windows Server 2008 R2.

## -remarks

The value specified by this enumeration indicates the relationship represented in the corresponding [SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX](./ns-winnt-system_logical_processor_information_ex.md)  structure. 


#### Examples

For an example, see <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation">GetLogicalProcessorInformation</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation">GetLogicalProcessorInformation</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_logical_processor_information">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>



<a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
