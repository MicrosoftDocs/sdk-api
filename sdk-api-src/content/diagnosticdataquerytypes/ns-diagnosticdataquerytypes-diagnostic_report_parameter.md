---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_REPORT_PARAMETER
title: DIAGNOSTIC_REPORT_PARAMETER
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_REPORT_PARAMETER, DIAGNOSTIC_REPORT_PARAMETER
description: Resource that describes the parameters for an error report.
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
req.typenames: DIAGNOSTIC_REPORT_PARAMETER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_REPORT_PARAMETER
 - DIAGNOSTIC_REPORT_PARAMETER
f1_keywords:
 - tagDIAGNOSTIC_REPORT_PARAMETER
 - diagnosticdataquerytypes/tagDIAGNOSTIC_REPORT_PARAMETER
 - DIAGNOSTIC_REPORT_PARAMETER
 - diagnosticdataquerytypes/DIAGNOSTIC_REPORT_PARAMETER
---

## -description

Resource that describes the parameters for an error report.

## -struct-fields

### -field name

Type: **[WCHAR\[\]](/windows/desktop/winprog/windows-data-types)**
The name of this parameter.

### -field value

Type: **[WCHAR\[\]](/windows/desktop/winprog/windows-data-types)**
The value of this parameter.

## -remarks

For more information about parameters, see the [**WER APIs**](/windows/win32/api/werapi/nf-werapi-werreportsetparameter).

## -see-also

