---
UID: NS:winnt._PROCESSOR_GROUP_INFO
title: PROCESSOR_GROUP_INFO (winnt.h)
description: Represents the number and affinity of processors in a processor group.
helpviewer_keywords: ["*PPROCESSOR_GROUP_INFO","PPROCESSOR_GROUP_INFO","PPROCESSOR_GROUP_INFO structure pointer","PROCESSOR_GROUP_INFO","PROCESSOR_GROUP_INFO structure","_PROCESSOR_GROUP_INFO","base.processor_group_info","winnt/PPROCESSOR_GROUP_INFO","winnt/PROCESSOR_GROUP_INFO"]
old-location: base\processor_group_info.htm
tech.root: backup
ms.assetid: 6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03
ms.date: 12/05/2018
ms.keywords: '*PPROCESSOR_GROUP_INFO, PPROCESSOR_GROUP_INFO, PPROCESSOR_GROUP_INFO structure pointer, PROCESSOR_GROUP_INFO, PROCESSOR_GROUP_INFO structure, _PROCESSOR_GROUP_INFO, base.processor_group_info, winnt/PPROCESSOR_GROUP_INFO, winnt/PROCESSOR_GROUP_INFO'
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
req.typenames: PROCESSOR_GROUP_INFO, *PPROCESSOR_GROUP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESSOR_GROUP_INFO
 - winnt/_PROCESSOR_GROUP_INFO
 - PPROCESSOR_GROUP_INFO
 - winnt/PPROCESSOR_GROUP_INFO
 - PROCESSOR_GROUP_INFO
 - winnt/PROCESSOR_GROUP_INFO
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
 - PROCESSOR_GROUP_INFO
---

# PROCESSOR_GROUP_INFO structure


## -description

Represents the number and affinity of processors in a processor group.

## -struct-fields

### -field MaximumProcessorCount

The maximum number of processors in the group.

### -field ActiveProcessorCount

The number of active processors in the group.

### -field Reserved

This member is reserved.

### -field ActiveProcessorMask

A bitmap that specifies the affinity for zero or more active processors within the group.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-group_relationship">GROUP_RELATIONSHIP</a>