---
UID: NE:werapi._WER_SUBMIT_RESULT
tech.root: wer
title: WER_SUBMIT_RESULT
ms.date: 07/21/2023
targetos: Windows
description: Defines the Windows Error Reporting (WER) submission result options.
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
 - _WER_SUBMIT_RESULT
 - PWER_SUBMIT_RESULT
 - WER_SUBMIT_RESULT
f1_keywords:
 - _WER_SUBMIT_RESULT
 - werapi/_WER_SUBMIT_RESULT
 - PWER_SUBMIT_RESULT
 - werapi/PWER_SUBMIT_RESULT
 - WER_SUBMIT_RESULT
 - werapi/WER_SUBMIT_RESULT
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_SUBMIT_RESULT
---

# WER_SUBMIT_RESULT enumeration

## -description

Defines the [Windows Error Reporting](../_wer/index.md) (WER) submission result options.

## -enum-fields

### -field WerReportQueued

Queued.

### -field WerReportUploaded

Uploaded.

### -field WerReportDebug

Debug.

### -field WerReportFailed

Failed.

### -field WerDisabled

Disabled.

### -field WerReportCancelled

Cancelled.

### -field WerDisabledQueue

Disabled queue.

### -field WerReportAsync

Async.

### -field WerCustomAction

Custom action.

### -field WerThrottled

Throttled.

### -field WerReportUploadedCab

Uploaded [Cabinet](/windows/win32/msi/cabinet-files) (CAB) file.

### -field WerStorageLocationNotFound

Storage location not found.

### -field WerSubmitResultMax

Submit the maximum data load.

## -remarks

## -see-also

[WerReportSubmit function](nf-werapi-werreportsubmit.md), [Windows Error Reporting](/windows/desktop/wer)
