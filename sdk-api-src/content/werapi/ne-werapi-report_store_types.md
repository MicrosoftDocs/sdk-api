---
UID: NE:werapi._REPORT_STORE_TYPES
tech.root: wer
title: REPORT_STORE_TYPES
description: Defines the types of Windows Error Reporting (WER) report stores that can be opened.
ms.date: 07/21/2023
targetos: Windows
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
 - _REPORT_STORE_TYPES
 - REPORT_STORE_TYPES
f1_keywords:
 - _REPORT_STORE_TYPES
 - werapi/_REPORT_STORE_TYPES
 - REPORT_STORE_TYPES
 - werapi/REPORT_STORE_TYPES
dev_langs:
 - c++
helpviewer_keywords:
 - _REPORT_STORE_TYPES
---

# REPORT_STORE_TYPES enumeration

## -description

Defines the types of [Windows Error Reporting](../_wer/index.md) (WER) report stores that can be opened.

## -enum-fields

### -field E_STORE_USER_ARCHIVE

User store of archived reports.

### -field E_STORE_USER_QUEUE

User store of queued reports.

### -field E_STORE_MACHINE_ARCHIVE

Machine-wide store of archived reports. You cannot depend on how long reports will be here. Older reports are better obtained through the event log.

### -field E_STORE_MACHINE_QUEUE

Machine-wide store of queued reports.

### -field E_STORE_INVALID

Invalid store archive.

## -remarks

## -see-also

[Windows Error Reporting](/windows/desktop/wer)
