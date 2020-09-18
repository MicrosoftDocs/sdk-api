---
UID: NE:amsi.AMSI_RESULT
title: AMSI_RESULT (amsi.h)
description: Specifies the types of results returned by scans.
helpviewer_keywords: ["AMSI_RESULT","AMSI_RESULT enumeration [Antimalware Scan Interface]","AMSI_RESULT_BLOCKED_BY_ADMIN_END","AMSI_RESULT_BLOCKED_BY_ADMIN_START","AMSI_RESULT_CLEAN","AMSI_RESULT_DETECTED","AMSI_RESULT_NOT_DETECTED","amsi.amsi_result","amsi/AMSI_RESULT","amsi/AMSI_RESULT_BLOCKED_BY_ADMIN_END","amsi/AMSI_RESULT_BLOCKED_BY_ADMIN_START","amsi/AMSI_RESULT_CLEAN","amsi/AMSI_RESULT_DETECTED","amsi/AMSI_RESULT_NOT_DETECTED"]
old-location: amsi\amsi_result.htm
tech.root: AMSI
ms.assetid: 3D7C74E3-BB09-4C53-930D-72D352374151
ms.date: 12/05/2018
ms.keywords: AMSI_RESULT, AMSI_RESULT enumeration [Antimalware Scan Interface], AMSI_RESULT_BLOCKED_BY_ADMIN_END, AMSI_RESULT_BLOCKED_BY_ADMIN_START, AMSI_RESULT_CLEAN, AMSI_RESULT_DETECTED, AMSI_RESULT_NOT_DETECTED, amsi.amsi_result, amsi/AMSI_RESULT, amsi/AMSI_RESULT_BLOCKED_BY_ADMIN_END, amsi/AMSI_RESULT_BLOCKED_BY_ADMIN_START, amsi/AMSI_RESULT_CLEAN, amsi/AMSI_RESULT_DETECTED, amsi/AMSI_RESULT_NOT_DETECTED
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AMSI_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AMSI_RESULT
 - amsi/AMSI_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amsi.h
api_name:
 - AMSI_RESULT
---

# AMSI_RESULT enumeration


## -description

The <b>AMSI_RESULT</b> enumeration specifies the types of results returned by scans.

## -enum-fields

### -field AMSI_RESULT_CLEAN

Known good. No detection found, and the result is likely not going to change after a future definition update.

### -field AMSI_RESULT_NOT_DETECTED

No detection found, but the result might change after a future definition update.

### -field AMSI_RESULT_BLOCKED_BY_ADMIN_START

Administrator policy blocked this content on this machine (beginning of range).

### -field AMSI_RESULT_BLOCKED_BY_ADMIN_END

Administrator policy blocked this content on this machine (end of range).

### -field AMSI_RESULT_DETECTED

Detection found. The content is considered malware  and should be blocked.

## -remarks

The antimalware provider may return a result between 1 and 32767, inclusive, as an estimated risk level. The larger the result, the riskier it is to continue with the content. These values are provider specific, and may indicate a malware family or ID.

Results within the range of <b>AMSI_RESULT_BLOCKED_BY_ADMIN_START</b> and <b>AMSI_RESULT_BLOCKED_BY_ADMIN_END</b> values (inclusive) are officially blocked by the admin specified policy. In these cases, the script in question will be blocked from executing. The range is large to accommodate future additions in functionality.

Any return result equal to or larger than 32768 is considered malware,  and the content should be blocked. An app should use <a href="/windows/desktop/api/amsi/nf-amsi-amsiresultismalware">AmsiResultIsMalware</a> to determine if this is the case.