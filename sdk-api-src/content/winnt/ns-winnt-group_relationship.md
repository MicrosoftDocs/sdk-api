---
UID: NS:winnt._GROUP_RELATIONSHIP
title: GROUP_RELATIONSHIP (winnt.h)
description: Represents information about processor groups. This structure is used with the GetLogicalProcessorInformationEx function.
helpviewer_keywords: ["*PGROUP_RELATIONSHIP","GROUP_RELATIONSHIP","GROUP_RELATIONSHIP structure","PGROUP_RELATIONSHIP","PGROUP_RELATIONSHIP structure pointer","_GROUP_RELATIONSHIP","base.group_relationship","winnt/GROUP_RELATIONSHIP","winnt/PGROUP_RELATIONSHIP"]
old-location: base\group_relationship.htm
tech.root: backup
ms.assetid: 3529ddef-04c5-4573-877d-c225da684e38
ms.date: 12/05/2018
ms.keywords: '*PGROUP_RELATIONSHIP, GROUP_RELATIONSHIP, GROUP_RELATIONSHIP structure, PGROUP_RELATIONSHIP, PGROUP_RELATIONSHIP structure pointer, _GROUP_RELATIONSHIP, base.group_relationship, winnt/GROUP_RELATIONSHIP, winnt/PGROUP_RELATIONSHIP'
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
req.typenames: GROUP_RELATIONSHIP, *PGROUP_RELATIONSHIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_RELATIONSHIP
 - winnt/_GROUP_RELATIONSHIP
 - PGROUP_RELATIONSHIP
 - winnt/PGROUP_RELATIONSHIP
 - GROUP_RELATIONSHIP
 - winnt/GROUP_RELATIONSHIP
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
 - GROUP_RELATIONSHIP
---

# GROUP_RELATIONSHIP structure


## -description

Represents information about processor groups. This structure is used with the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function.

## -struct-fields

### -field MaximumGroupCount

The maximum number of processor groups on the system.

### -field ActiveGroupCount

The number of active groups on the system. This member indicates the number of <a href="/windows/desktop/api/winnt/ns-winnt-processor_group_info">PROCESSOR_GROUP_INFO</a> structures in the <b>GroupInfo</b> array.

### -field Reserved

This member is reserved.

### -field GroupInfo

An array of <a href="/windows/desktop/api/winnt/ns-winnt-processor_group_info">PROCESSOR_GROUP_INFO</a> structures. Each structure represents the number and affinity of processors in an active group on the system.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_group_info">PROCESSOR_GROUP_INFO</a>



<a href="/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>