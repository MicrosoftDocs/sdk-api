---
UID: NE:werapi._WER_FILE_TYPE
tech.root: wer
title: WER_FILE_TYPE
ms.date: 07/21/2023
targetos: Windows
description: Defines the possible Windows Error Reporting (WER) file types for the minidump report.
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
 - _WER_FILE_TYPE
 - WER_FILE_TYPE
f1_keywords:
 - _WER_FILE_TYPE
 - werapi/_WER_FILE_TYPE
 - WER_FILE_TYPE
 - werapi/WER_FILE_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_FILE_TYPE
---

# WER_FILE_TYPE enumeration

## -description

Defines the possible [Windows Error Reporting](../_wer/index.md) (WER) file types for the minidump report.

## -enum-fields

### -field WerFileTypeMicrodump

Micro dump.

### -field WerFileTypeMinidump

Mini dump.

### -field WerFileTypeHeapdump

Heap dump.

### -field WerFileTypeUserDocument

User document.

### -field WerFileTypeOther

Other.

### -field WerFileTypeTriagedump

Triage dump.

### -field WerFileTypeCustomDump

Custom dump.

### -field WerFileTypeAuxiliaryDump

Auxiliary dump.

### -field WerFileTypeEtlTrace

Event Trace Logging (ETL) trace.

### -field WerFileTypeAuxiliaryHeapDump

Auxiliary heap dump.

### -field WerFileTypeMax

Maximum data dump.

## -remarks

## -see-also

[WerReportAddFile function](nf-werapi-werreportaddfile.md), [Windows Error Reporting](/windows/desktop/wer)
