---
UID: NS:werapi._WER_REPORT_INFORMATION_V4
tech.root: 
title: WER_REPORT_INFORMATION_V4
ms.date: 
targetos: Windows
description: 
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
req.typenames: WER_REPORT_INFORMATION_V4, *PWER_REPORT_INFORMATION_V4
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
 - _WER_REPORT_INFORMATION_V4
 - PWER_REPORT_INFORMATION_V4
 - WER_REPORT_INFORMATION_V4
f1_keywords:
 - _WER_REPORT_INFORMATION_V4
 - werapi/_WER_REPORT_INFORMATION_V4
 - PWER_REPORT_INFORMATION_V4
 - werapi/PWER_REPORT_INFORMATION_V4
 - WER_REPORT_INFORMATION_V4
 - werapi/WER_REPORT_INFORMATION_V4
dev_langs:
 - c++
helpviewer_keywords:
 - _WER_REPORT_INFORMATION_V4
---

## -description

## -struct-fields

### -field dwSize

### -field hProcess

### -field wzConsentKey[64]

### -field wzFriendlyEventName[128]

### -field wzApplicationName[128]

### -field wzApplicationPath[MAX_PATH]

### -field wzDescription[512]

### -field hwndParent

### -field wzNamespacePartner[64]

### -field wzNamespaceGroup[64]

### -field rgbApplicationIdentity[16]

### -field hSnapshot

### -field hDeleteFilesImpersonationToken

## -remarks

## -see-also

