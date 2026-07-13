---
UID: NF:werapi.WerReportSetParameter
title: WerReportSetParameter function (werapi.h)
description: Sets the parameters that uniquely identify an event for the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WER_P0","WER_P1","WER_P2","WER_P3","WER_P4","WER_P5","WER_P6","WER_P7","WER_P8","WER_P9","WerReportSetParameter","WerReportSetParameter function [Windows Error Reporting]","base.werreportsetparameter","wer.werreportsetparameter","werapi/WerReportSetParameter"]
old-location: wer\werreportsetparameter.htm
tech.root: wer
ms.assetid: accf423d-6f03-41e2-b5e9-4a0b630bc918
ms.date: 07/25/2023
ms.keywords: WER_P0, WER_P1, WER_P2, WER_P3, WER_P4, WER_P5, WER_P6, WER_P7, WER_P8, WER_P9, WerReportSetParameter, WerReportSetParameter function [Windows Error Reporting], base.werreportsetparameter, wer.werreportsetparameter, werapi/WerReportSetParameter
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerReportSetParameter
 - werapi/WerReportSetParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportSetParameter
---

# WerReportSetParameter function

## -description

Sets the parameters that uniquely identify an event for the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

### -param dwparamID [in]

The identifier of the parameter to be set. This parameter can be one of the following values.

- WER_P0
- WER_P1
- WER_P2
- WER_P3
- WER_P4
- WER_P5
- WER_P6
- WER_P7
- WER_P8
- WER_P9

### -param pwzName [in, optional]

A pointer to a Unicode string that contains the name of the parameter. If this parameter is **NULL**, the default name is P*x*, where *x* matches the integer portion of the value specified in *dwparamID*.

### -param pwzValue [in]

The parameter value.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**E_HANDLE**|The specified handle is not valid.|
|**WER_E_LENGTH_EXCEEDED**|The length of one or more string arguments has exceeded its limit.|

## -remarks

Each report supports parameters P0 through P9. This function sets one parameter at a time. If parameter P*x* is set, then all parameters from P0 and P*x* must be set.

## -see-also

[WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
