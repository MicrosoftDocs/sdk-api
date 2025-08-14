---
UID: NF:werapi.WerReportCreate
title: WerReportCreate function (werapi.h)
description: Creates a Windows Error Reporting (WER) report that describes an application event.
helpviewer_keywords: ["WerReportApplicationCrash","WerReportApplicationHang","WerReportCreate","WerReportCreate function [Windows Error Reporting]","WerReportCritical","WerReportInvalid","WerReportKernel","WerReportNonCritical","base.werreportcreate","wer.werreportcreate","werapi/WerReportCreate"]
old-location: wer\werreportcreate.htm
tech.root: wer
ms.assetid: 41f68dde-5e43-45a6-8e0b-3ae0c6180e8b
ms.date: 07/25/2023
ms.keywords: WerReportApplicationCrash, WerReportApplicationHang, WerReportCreate, WerReportCreate function [Windows Error Reporting], WerReportCritical, WerReportInvalid, WerReportKernel, WerReportNonCritical, base.werreportcreate, wer.werreportcreate, werapi/WerReportCreate
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
 - WerReportCreate
 - werapi/WerReportCreate
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
 - WerReportCreate
---

# WerReportCreate function

## -description

Creates a [Windows Error Reporting](../_wer/index.md) (WER) report that describes an application event.

## -parameters

### -param pwzEventType [in]

A pointer to a Unicode string that specifies the name of the event.

### -param repType [in]

The type of report. This parameter can be one of the following values from the **WER_REPORT_TYPE** enumeration type.

|Value|Meaning|
|--- |--- |
|**WerReportApplicationCrash**<br/>2|An error that has caused the application to stop running has occurred.|
|**WerReportApplicationHang**<br/>3|An error that has caused the application to stop responding has occurred.|
|**WerReportInvalid**<br/>5|An error that has called out a return that is not valid has occurred.|
|**WerReportKernel**<br/>4|An error in the kernel has occurred.|
|**WerReportCritical**<br/>1|A critical error, such as a crash or non-response, has occurred. By default, processes that experience a critical error are terminated or restarted.|
|**WerReportNonCritical**<br/>0|An error that is not critical has occurred. This type of report shows no UI; the report is silently queued. It may then be sent silently to the server in the background if adequate user consent is available.|

### -param pReportInformation [in, optional]

A pointer to a [WER_REPORT_INFORMATION](/windows/desktop/api/werapi/ns-werapi-wer_report_information) structure that specifies information for the report.

### -param phReportHandle [out]

A handle to the report. If the function fails, this handle is **NULL**.

## -returns

This function returns **S_OK** on success or an error code on failure.

## -remarks

Use the following functions to specify additional information to be submitted:

- [WerReportAddDump](/windows/desktop/api/werapi/nf-werapi-werreportadddump)
- [WerReportAddFile](/windows/desktop/api/werapi/nf-werapi-werreportaddfile)
- [WerReportSetParameter](/windows/desktop/api/werapi/nf-werapi-werreportsetparameter)

To submit the information, call the [WerReportSubmit](/windows/desktop/api/werapi/nf-werapi-werreportsubmit) function. When you have finished with the report handle, call the [WerReportCloseHandle](/windows/desktop/api/werapi/nf-werapi-werreportclosehandle) function.

Applications can also indicate that they would like the opportunity to recover data or restart on failure. For more information, see [Application Recovery and Restart](/windows/desktop/wsw/portal).

To view the reports submitted by your application, go to Windows Quality Online Services.

## -see-also

[Application Recovery and Restart](/windows/desktop/wsw/portal), [WER_REPORT_INFORMATION](/windows/desktop/api/werapi/ns-werapi-wer_report_information), [WerReportCloseHandle](/windows/desktop/api/werapi/nf-werapi-werreportclosehandle), [WerReportSubmit](/windows/desktop/api/werapi/nf-werapi-werreportsubmit), [Windows Error Reporting](/windows/desktop/wer)
