---
UID: NS:winnt._CONTEXT~r1
tech.root: Debug
title: CONTEXT (Arm32)
ms.date: 03/24/2025
targetos: Windows
description: Contains processor-specific register data for Arm32 architecture. The system uses CONTEXT structures to perform various internal operations.
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
req.typenames: CONTEXT, *PCONTEXT
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
 - PCONTEXT
 - CONTEXT
f1_keywords:
 - _CONTEXT
 - winnt/_CONTEXT
 - PCONTEXT
 - winnt/PCONTEXT
 - CONTEXT
 - winnt/CONTEXT
dev_langs:
 - c++
helpviewer_keywords:
 - _CONTEXT
h1-override: CONTEXT structure (Arm32)
---

# CONTEXT structure (Arm32)

## -description

Contains processor-specific register data. The system uses <b>CONTEXT</b> structures to perform various internal operations. The structure definition varies for different processor architectures. This page applies to the Arm32 architecture. The following table links to the structures for other architectures.

| Architecture | API reference page |
|--------------|--------------------|
| x86 64-bit | [CONTEXT structure (x86 64-bit)](ns-winnt-context.md) |
| x86 32-bit | [CONTEXT structure (x86 32-bit)](ns-winnt-context~r2.md) |
| Arm64 | [ARM64_NT_CONTEXT structure](ns-winnt-arm64_nt_context.md) |


## -struct-fields

### -field ContextFlags

### -field R0

### -field R1

### -field R2

### -field R3

### -field R4

### -field R5

### -field R6

### -field R7

### -field R8

### -field R9

### -field R10

### -field R11

### -field R12

### -field Sp

### -field Lr

### -field Pc

### -field Cpsr

### -field Fpscr

### -field Padding

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Q[16]

### -field DUMMYUNIONNAME.D[32]

### -field DUMMYUNIONNAME.S[32]

### -field Bvr[ARM_MAX_BREAKPOINTS]

### -field Bcr[ARM_MAX_BREAKPOINTS]

### -field Wvr[ARM_MAX_WATCHPOINTS]

### -field Wcr[ARM_MAX_WATCHPOINTS]

### -field Padding2[2]

## -remarks

## -see-also

