---
UID: NS:winnt._PROCESSOR_NUMBER
title: PROCESSOR_NUMBER (winnt.h)
description: Represents a logical processor in a processor group.
helpviewer_keywords: ["*PPROCESSOR_NUMBER","PPROCESSOR_NUMBER","PPROCESSOR_NUMBER structure pointer","PROCESSOR_NUMBER","PROCESSOR_NUMBER structure","base.processor_number","winnt/PPROCESSOR_NUMBER","winnt/PROCESSOR_NUMBER"]
old-location: base\processor_number.htm
tech.root: backup
ms.assetid: 9005c6d4-07a9-4ce0-9ee2-54880d7244c3
ms.date: 12/05/2018
ms.keywords: '*PPROCESSOR_NUMBER, PPROCESSOR_NUMBER, PPROCESSOR_NUMBER structure pointer, PROCESSOR_NUMBER, PROCESSOR_NUMBER structure, base.processor_number, winnt/PPROCESSOR_NUMBER, winnt/PROCESSOR_NUMBER'
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
req.typenames: PROCESSOR_NUMBER, *PPROCESSOR_NUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESSOR_NUMBER
 - winnt/_PROCESSOR_NUMBER
 - PPROCESSOR_NUMBER
 - winnt/PPROCESSOR_NUMBER
 - PROCESSOR_NUMBER
 - winnt/PROCESSOR_NUMBER
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
 - PROCESSOR_NUMBER
---

# PROCESSOR_NUMBER structure


## -description

Represents a logical processor in a processor group.

## -struct-fields

### -field Group

The processor group to which the logical processor is assigned.

### -field Number

The number of the logical processor relative to the group.

### -field Reserved

This parameter is reserved.

## -see-also

<a href="/windows/desktop/ProcThread/processor-groups">Processor Groups</a>