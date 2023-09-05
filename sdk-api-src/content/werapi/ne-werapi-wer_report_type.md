---
UID: NE:werapi._WER_REPORT_TYPE
tech.root: wer
title: WER_REPORT_TYPE
ms.date: 07/21/2023
targetos: Windows
description: Defines the Windows Error Reporting (WER) report types.
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
 - _WER_REPORT_TYPE
 - WER_REPORT_TYPE
f1_keywords:
 - _WER_REPORT_TYPE
 - werapi/_WER_REPORT_TYPE
 - WER_REPORT_TYPE
 - werapi/WER_REPORT_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_REPORT_TYPE
---

# WER_REPORT_TYPE enumeration

## -description

Defines the [Windows Error Reporting](../_wer/index.md) (WER) report types.

## -enum-fields

### -field WerReportNonCritical

Non-critical.

### -field WerReportCritical

Critical.

### -field WerReportApplicationCrash

Application crash.

### -field WerReportApplicationHang

Application hang.

### -field WerReportKernel

Kernel.

### -field WerReportInvalid

Invalid.

## -remarks

## -see-also

[WerReportCreate function](nf-werapi-werreportcreate.md), [Windows Error Reporting](../_wer/index.md)
