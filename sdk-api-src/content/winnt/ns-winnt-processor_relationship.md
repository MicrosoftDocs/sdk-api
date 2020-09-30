---
UID: NS:winnt._PROCESSOR_RELATIONSHIP
title: PROCESSOR_RELATIONSHIP (winnt.h)
description: Represents information about affinity within a processor group. This structure is used with the GetLogicalProcessorInformationEx function.
helpviewer_keywords: ["*PPROCESSOR_RELATIONSHIP","PPROCESSOR_RELATIONSHIP","PPROCESSOR_RELATIONSHIP structure pointer","PROCESSOR_RELATIONSHIP","PROCESSOR_RELATIONSHIP structure","_PROCESSOR_RELATIONSHIP","base.processor_relationship","winnt/PPROCESSOR_RELATIONSHIP","winnt/PROCESSOR_RELATIONSHIP"]
old-location: base\processor_relationship.htm
tech.root: backup
ms.assetid: 1efda80d-cf5b-4312-801a-ea3585b152ac
ms.date: 12/05/2018
ms.keywords: '*PPROCESSOR_RELATIONSHIP, PPROCESSOR_RELATIONSHIP, PPROCESSOR_RELATIONSHIP structure pointer, PROCESSOR_RELATIONSHIP, PROCESSOR_RELATIONSHIP structure, _PROCESSOR_RELATIONSHIP, base.processor_relationship, winnt/PPROCESSOR_RELATIONSHIP, winnt/PROCESSOR_RELATIONSHIP'
req.header: winnt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROCESSOR_RELATIONSHIP, *PPROCESSOR_RELATIONSHIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESSOR_RELATIONSHIP
 - winnt/_PROCESSOR_RELATIONSHIP
 - PPROCESSOR_RELATIONSHIP
 - winnt/PPROCESSOR_RELATIONSHIP
 - PROCESSOR_RELATIONSHIP
 - winnt/PROCESSOR_RELATIONSHIP
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
 - PROCESSOR_RELATIONSHIP
---

# PROCESSOR_RELATIONSHIP structure


## -description

Represents information about affinity within a processor group. This structure is used with the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function.

## -struct-fields

### -field Flags

If the <b>Relationship</b> member of the <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorCore</b>, this member is LTP_PC_SMT if the core has more than one logical processor, or 0 if the core has one logical processor. 

If the <b>Relationship</b> member of the <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorPackage</b>, this member is always 0.

### -field EfficiencyClass

 If the <b>Relationship</b> member of the <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorCore</b>, <b>EfficiencyClass</b> specifies the intrinsic tradeoff between performance and power for the applicable core. A core  with a higher value for the efficiency class has intrinsically greater performance and less efficiency than a core with a lower value for the efficiency class. <b>EfficiencyClass</b> is only nonzero on systems with a heterogeneous set of cores.

If the <b>Relationship</b> member of the <a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorPackage</b>, <b>EfficiencyClass</b> is always 0.

The minimum operating system version that supports this member is Windows 10.

### -field Reserved

This member is reserved.

### -field GroupCount

This member specifies the number of entries in the <b>GroupMask</b> array. For more information, see Remarks.

### -field GroupMask

An array of <a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structures. The <b>GroupCount</b> member specifies the number of structures in the array. Each structure in the array specifies a  group number and processor affinity within the group.

## -remarks

The <b>PROCESSOR_RELATIONSHIP</b> structure describes the logical processors associated with either a processor core or a processor package.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor core, the <b>GroupCount</b> member is always 1.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor package, the  <b>GroupCount</b> member is 1 only if all processors are in the same processor group. If the package contains more than one NUMA node, the system might assign different NUMA nodes to different processor groups. In this case, the <b>GroupCount</b> member is the number of groups to which NUMA nodes in the package are assigned.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a>



<a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>