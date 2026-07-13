---
UID: NS:winnt._CONTEXT~r2
tech.root: Debug
title: CONTEXT (x86 32-bit)
ms.date: 03/24/2025
targetos: Windows
description: Contains processor-specific register data for 32-bit x86 architecture. The system uses CONTEXT structures to perform various internal operations.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: CONTEXT
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _CONTEXT
 - CONTEXT
f1_keywords:
 - _CONTEXT
 - winnt/_CONTEXT
 - CONTEXT
 - winnt/CONTEXT
dev_langs:
 - c++
helpviewer_keywords:
 - _CONTEXT
h1-override: CONTEXT (x86 32-bit)
---

# CONTEXT (x86 32-bit)

## -description

Contains processor-specific register data. The system uses <b>CONTEXT</b> structures to perform various internal operations. The structure definition varies for different processor architectures. This page applies to the 32-bit x86 architecture. The following table links to the structures for other architectures.

| Architecture | API reference page |
|--------------|--------------------|
| x86 64-bit | [CONTEXT structure (x86 64-bit)](ns-winnt-context.md) |
| Arm32 | [CONTEXT structure (Arm32)](ns-winnt-context~r1.md) |
| Arm64 | [ARM64_NT_CONTEXT structure](ns-winnt-arm64_nt_context.md) |


## -struct-fields

### -field ContextFlags

### -field Dr0

### -field Dr1

### -field Dr2

### -field Dr3

### -field Dr6

### -field Dr7

### -field FloatSave

### -field SegGs

### -field SegFs

### -field SegEs

### -field SegDs

### -field Edi

### -field Esi

### -field Ebx

### -field Edx

### -field Ecx

### -field Eax

### -field Ebp

### -field Eip

### -field SegCs

### -field EFlags

### -field Esp

### -field SegSs

### -field ExtendedRegisters[MAXIMUM_SUPPORTED_EXTENSION]

## -remarks

## -see-also

