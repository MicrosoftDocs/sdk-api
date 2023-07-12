---
UID: NE:werapi._WER_CONSENT
tech.root: 
title: WER_CONSENT
ms.date: 
targetos: Windows
description: 
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
 - _WER_CONSENT
 - WER_CONSENT
f1_keywords:
 - _WER_CONSENT
 - werapi/_WER_CONSENT
 - WER_CONSENT
 - werapi/WER_CONSENT
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_CONSENT
---

# WER_CONSENT enumeration

## -description

Specifies the possible Windows Error Reporting (WER) user consent states.

## -enum-fields

### -field WerConsentNotAsked:1

User was not asked for consent.

### -field WerConsentApproved:2

User approved consent.

### -field WerConsentDenied:3

User denied consent.

### -field WerConsentAlwaysPrompt:4

User is always asked for consent.

### -field WerConsentMax:5

The maximum value for this enumeration.

## -remarks

## -see-also

[WerReportSubmit function](nf-werapi-werreportsubmit.md)