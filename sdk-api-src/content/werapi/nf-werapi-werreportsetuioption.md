---
UID: NF:werapi.WerReportSetUIOption
title: WerReportSetUIOption function (werapi.h)
description: Sets the user interface options for the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WerReportSetUIOption","WerReportSetUIOption function [Windows Error Reporting]","WerUIAdditionalDataDlgHeader","WerUICloseDlgBody","WerUICloseDlgButtonText","WerUICloseDlgHeader","WerUICloseText","WerUIConsentDlgBody","WerUIConsentDlgHeader","WerUIIconFilePath","WerUIOfflineSolutionCheckText","WerUIOnlineSolutionCheckText","base.werreportsetuioption","wer.werreportsetuioption","werapi/WerReportSetUIOption"]
old-location: wer\werreportsetuioption.htm
tech.root: wer
ms.assetid: c8816782-faec-490e-898f-a40df8fb205b
ms.date: 07/25/2023
ms.keywords: WerReportSetUIOption, WerReportSetUIOption function [Windows Error Reporting], WerUIAdditionalDataDlgHeader, WerUICloseDlgBody, WerUICloseDlgButtonText, WerUICloseDlgHeader, WerUICloseText, WerUIConsentDlgBody, WerUIConsentDlgHeader, WerUIIconFilePath, WerUIOfflineSolutionCheckText, WerUIOnlineSolutionCheckText, base.werreportsetuioption, wer.werreportsetuioption, werapi/WerReportSetUIOption
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
 - WerReportSetUIOption
 - werapi/WerReportSetUIOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wer.dll
api_name:
 - WerReportSetUIOption
---

# WerReportSetUIOption function

## -description

Sets the user interface options for the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

### -param repUITypeID [in]

The user interface element to be customized. This parameter can be one of the following values from the **WER_REPORT_UI** enumeration type.

|Value|Meaning|
|--- |--- |
|**WerUIAdditionalDataDlgHeader**|The instructions for the additional data dialog box.|
|**WerUICloseDlgBody**|The contents of the close dialog box.|
|**WerUICloseDlgButtonText**|The text for the button in the close dialog box.|
|**WerUICloseDlgHeader**|The main instructions for the close dialog box.|
|**WerUICloseText**|The text for the link to just terminate the application.|
|**WerUIConsentDlgBody**|The contents of the consent dialog box.|
|**WerUIConsentDlgHeader**|The main instructions for the consent dialog box.|
|**WerUIIconFilePath**|The icon to be displayed in the consent dialog box.|
|**WerUIOfflineSolutionCheckText**|The text for the link to check for a solution when offline.|
|**WerUIOnlineSolutionCheckText**|The text for the link to check for a solution when online.|

### -param pwzValue [in]

A pointer to a Unicode string that specifies the custom text. For more information, see the description of *repUITypeID*.

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also

[WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
