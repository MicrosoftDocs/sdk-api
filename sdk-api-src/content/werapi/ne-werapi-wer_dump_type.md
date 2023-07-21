---
UID: NE:werapi._WER_DUMP_TYPE
tech.root: wer
title: WER_DUMP_TYPE
ms.date: 07/21/2023
targetos: Windows
description: Defines the possible Windows Error Reporting (WER) minidump types. 
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: werapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - werapi.h
api_name:
 - _WER_DUMP_TYPE
 - WER_DUMP_TYPE
f1_keywords:
 - _WER_DUMP_TYPE
 - werapi/_WER_DUMP_TYPE
 - WER_DUMP_TYPE
 - werapi/WER_DUMP_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_DUMP_TYPE
---

# WER_DUMP_TYPE enumeration

## -description

Defines the possible [Windows Error Reporting](../_wer/index.md) (WER) [minidump](/windows/desktop/Debug/minidump-files) types.

## -enum-fields

### -field WerDumpTypeNone

No dump.

### -field WerDumpTypeMicroDump

A limited minidump that contains only a stack trace. This type is equivalent to creating a minidump with the following options:

- MiniDumpWithDataSegs
- MiniDumpWithUnloadedModules
- MiniDumpWithProcessThreadData
- MiniDumpWithoutOptionalData

### -field WerDumpTypeMiniDump

A minidump. This type is equivalent to creating a minidump with the following options:

- MiniDumpWithDataSegs
- MiniDumpWithUnloadedModules
- MiniDumpWithProcessThreadData
- MiniDumpWithTokenInformation (Windows 7 and later)

### -field WerDumpTypeHeapDump

An extended minidump that contains additional data such as the process memory. This type is equivalent to creating a minidump with the following options:

- MiniDumpWithDataSegs
- MiniDumpWithProcessThreadData
- MiniDumpWithHandleData
- MiniDumpWithPrivateReadWriteMemory
- MiniDumpWithUnloadedModules
- MiniDumpWithFullMemoryInfo
- MiniDumpWithThreadInfo (Windows 7 and later)
- MiniDumpWithTokenInformation (Windows 7 and later)
- MiniDumpWithPrivateWriteCopyMemory (Windows 7 and later)

### -field WerDumpTypeTriageDump

An extended minidump that contains additional data for triage purposes.

### -field WerDumpTypeMax

An extended minidump that contains all saved data.

## -remarks

## -see-also

[WerReportAddDump function](nf-werapi-werreportadddump.md), [Windows Error Reporting](/windows/desktop/wer)
