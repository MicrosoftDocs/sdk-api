---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_REPORT_SIGNATURE
title: DIAGNOSTIC_REPORT_SIGNATURE
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_REPORT_SIGNATURE, DIAGNOSTIC_REPORT_SIGNATURE
description: This resource describes the signature for a diagnostic report.
tech.root: security
targetos: Windows
ms.service: windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquerytypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: DIAGNOSTIC_REPORT_SIGNATURE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_REPORT_SIGNATURE
 - DIAGNOSTIC_REPORT_SIGNATURE
f1_keywords:
 - tagDIAGNOSTIC_REPORT_SIGNATURE
 - diagnosticdataquerytypes/tagDIAGNOSTIC_REPORT_SIGNATURE
 - DIAGNOSTIC_REPORT_SIGNATURE
 - diagnosticdataquerytypes/DIAGNOSTIC_REPORT_SIGNATURE
---

## -description

This resource describes the signature for a diagnostic report.

## -struct-fields

### -field eventName

Type: **[WCHAR\[\]](/windows/desktop/winprog/windows-data-types)**
A string that specifies the name of this application event.

### -field parameters

Type: **[DIAGNOSTIC_DATA_REPORT_PARAMETER\[\]](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_report_parameter)**
A list of parameters for this report.

## -remarks

## -see-also

