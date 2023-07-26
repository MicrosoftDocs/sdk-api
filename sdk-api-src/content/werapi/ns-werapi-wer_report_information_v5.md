---
UID: NS:werapi._WER_REPORT_INFORMATION_V5
tech.root: wer
title: WER_REPORT_INFORMATION_V5
ms.date: 07/21/2023
targetos: Windows
description: Contains Windows Error Reporting (WER) information used by the WerReportCreate function.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: werapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: WER_REPORT_INFORMATION_V5, *PWER_REPORT_INFORMATION_V5
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - werapi.h
api_name:
 - _WER_REPORT_INFORMATION_V5
 - PWER_REPORT_INFORMATION_V5
 - WER_REPORT_INFORMATION_V5
f1_keywords:
 - _WER_REPORT_INFORMATION_V5
 - werapi/_WER_REPORT_INFORMATION_V5
 - PWER_REPORT_INFORMATION_V5
 - werapi/PWER_REPORT_INFORMATION_V5
 - WER_REPORT_INFORMATION_V5
 - werapi/WER_REPORT_INFORMATION_V5
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_REPORT_INFORMATION_V5
---

# WER_REPORT_INFORMATION_V5 function

## -description

Contains [Windows Error Reporting](../_wer/index.md) (WER) information used by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

## -struct-fields

### -field dwSize

The size of this structure, in bytes.

### -field hProcess

A handle to the process for which the report is being generated. If this member is **NULL**, this is the calling process.

### -field wzConsentKey[64]

### -field wzFriendlyEventName[128]

### -field wzApplicationName[128]

### -field wzApplicationPath[MAX_PATH]

### -field wzDescription[512]

### -field hwndParent

A handle to the parent window.

### -field wzNamespacePartner[64]

### -field wzNamespaceGroup[64]

### -field rgbApplicationIdentity[16]

### -field hSnapshot

### -field hDeleteFilesImpersonationToken

### -field submitResultMax

## -remarks

## -see-also

[WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](../_wer/index.md)
