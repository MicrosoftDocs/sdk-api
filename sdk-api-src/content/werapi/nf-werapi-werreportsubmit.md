---
UID: NF:werapi.WerReportSubmit
title: WerReportSubmit function (werapi.h)
description: Submits the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WER_SUBMIT_ADD_REGISTERED_DATA","WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY","WER_SUBMIT_BYPASS_DATA_THROTTLING","WER_SUBMIT_HONOR_RECOVERY","WER_SUBMIT_HONOR_RESTART","WER_SUBMIT_NO_ARCHIVE","WER_SUBMIT_NO_CLOSE_UI","WER_SUBMIT_NO_QUEUE","WER_SUBMIT_OUTOFPROCESS","WER_SUBMIT_OUTOFPROCESS_ASYNC","WER_SUBMIT_QUEUE","WER_SUBMIT_REPORT_MACHINE_ID","WER_SUBMIT_SHOW_DEBUG","WER_SUBMIT_START_MINIMIZED","WerConsentAlwaysPrompt","WerConsentApproved","WerConsentDenied","WerConsentMax","WerConsentNotAsked","WerCustomAction","WerDisabled","WerDisabledQueue","WerReportAsync","WerReportCancelled","WerReportDebug","WerReportFailed","WerReportQueued","WerReportSubmit","WerReportSubmit function [Windows Error Reporting]","WerReportUploaded","base.werreportsubmit","wer.werreportsubmit","werapi/WerReportSubmit"]
old-location: wer\werreportsubmit.htm
tech.root: wer
ms.assetid: 1433862e-5cf6-4d31-9fd9-137b7b86ec57
ms.date: 07/26/2023
ms.keywords: WER_SUBMIT_ADD_REGISTERED_DATA, WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY, WER_SUBMIT_BYPASS_DATA_THROTTLING, WER_SUBMIT_HONOR_RECOVERY, WER_SUBMIT_HONOR_RESTART, WER_SUBMIT_NO_ARCHIVE, WER_SUBMIT_NO_CLOSE_UI, WER_SUBMIT_NO_QUEUE, WER_SUBMIT_OUTOFPROCESS, WER_SUBMIT_OUTOFPROCESS_ASYNC, WER_SUBMIT_QUEUE, WER_SUBMIT_REPORT_MACHINE_ID, WER_SUBMIT_SHOW_DEBUG, WER_SUBMIT_START_MINIMIZED, WerConsentAlwaysPrompt, WerConsentApproved, WerConsentDenied, WerConsentMax, WerConsentNotAsked, WerCustomAction, WerDisabled, WerDisabledQueue, WerReportAsync, WerReportCancelled, WerReportDebug, WerReportFailed, WerReportQueued, WerReportSubmit, WerReportSubmit function [Windows Error Reporting], WerReportUploaded, base.werreportsubmit, wer.werreportsubmit, werapi/WerReportSubmit
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
 - WerReportSubmit
 - werapi/WerReportSubmit
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
 - WerReportSubmit
---

# WerReportSubmit function

## -description

Submits the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [**WerReportCreate**](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

### -param consent [in]

The consent status. This parameter can be one of the following values from the [**WER_CONSENT**](ne-werapi-wer_consent.md) enumeration type.

|Value|Meaning|
|--- |--- |
|**WerConsentAlwaysPrompt**<br/>4|The user is always asked to submit the request.|
|**WerConsentApproved**<br/>2|The user has approved the submission request.|
|**WerConsentDenied**<br/>3|The user has denied the submission request.|
|**WerConsentMax**<br/>5|The maximum value for the **WER_CONSENT** enumeration type.|
|**WerConsentNotAsked**<br/>1|The user was not asked for consent.|

### -param dwFlags [in]

This parameter can be one or more of the following values.

|Value|Meaning|
|--- |--- |
|**WER_SUBMIT_ADD_REGISTERED_DATA**<br/>16|Add the data registered by [WerSetFlags](/windows/desktop/api/werapi/nf-werapi-wersetflags), [WerRegisterFile](nf-werapi-werregisterfile.md), and [WerRegisterMemoryBlock](nf-werapi-werregistermemoryblock.md) to the report.|
|**WER_SUBMIT_HONOR_RECOVERY**<br/>1|Honor any recovery registration for the application. For more information, see [RegisterApplicationRecoveryCallback](../winbase/nf-winbase-registerapplicationrecoverycallback.md).|
|**WER_SUBMIT_HONOR_RESTART**<br/>2|Honor any restart registration for the application. For more information, see [RegisterApplicationRestart](../winbase/nf-winbase-registerapplicationrecoverycallback.md).|
|**WER_SUBMIT_NO_ARCHIVE**<br/>256|Do not archive the report.|
|**WER_SUBMIT_NO_CLOSE_UI**<br/>64|Do not display the close dialog box for the critical report.|
|**WER_SUBMIT_NO_QUEUE**<br/>128|Do not queue the report. If there is adequate user consent the report is sent to Microsoft immediately; otherwise, the report is discarded. You may use this flag for non-critical reports.<br/><br/>The report is discarded for any action that would require the report to be queued. For example, if the computer is offline when you submit the report, the report is discarded. Also, if there is insufficient consent (for example, consent was required for the data portion of the report), the report is discarded.|
|**WER_SUBMIT_OUTOFPROCESS**<br/>32|Spawn another process to submit the report. The calling thread is blocked until the function returns.<br/><br/>**NOTE:** Window messages will be pumped so that UI activity on the calling thread is not blocked.|
|**WER_SUBMIT_OUTOFPROCESS_ASYNC**<br/>1024|Spawn another process to submit the report and return from this function call immediately. Note that the contents of the *pSubmitResult* parameter are undefined and there is no way to query when the reporting completes or the completion status.|
|**WER_SUBMIT_QUEUE**<br/>4|Add the report to the WER queue without notifying the user.  The report is queued only—reporting (sending the report to Microsoft) occurs later based on the user's consent level.|
|**WER_SUBMIT_SHOW_DEBUG**<br/>8|Show the debug button.|
|**WER_SUBMIT_START_MINIMIZED**<br/>512|The initial UI is minimized and flashing.|
|**WER_SUBMIT_BYPASS_DATA_THROTTLING**<br/>2048|Bypass data throttling for the report.<br/><br/>**Windows 7 or earlier:** This parameter is not available.|
|**WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY**<br/>4096|Archive only the parameters; the cab is discarded. This flag overrides the [ConfigureArchive](/windows/desktop/wer/wer-settings) WER setting.<br/><br/>**Windows 7 or earlier:** This parameter is not available.|
|**WER_SUBMIT_REPORT_MACHINE_ID**<br/>8192|Always send the unique, 128-bit computer identifier with the report, regardless of the consent with which the report was submitted. See Remarks for additional information.<br/><br/>**Windows 7 or earlier:** This parameter is not available.|

### -param pSubmitResult [out, optional]

The result of the submission. This parameter can be one of the following values from the **WER_SUBMIT_RESULT** enumeration type.

|Value|Meaning|
|--- |--- |
|**WerCustomAction**<br/>9|Error reporting can be customized.|
|**WerDisabled**<br/>5|Error reporting was disabled.|
|**WerDisabledQueue**<br/>7|Queuing was disabled.|
|**WerReportAsync**<br/>8|The report was asynchronous.|
|**WerReportCancelled**<br/>6|The report was canceled.|
|**WerReportDebug**<br/>3|The Debug button was clicked.|
|**WerReportFailed**<br/>4|The report submission failed.|
|**WerReportQueued**<br/>1|The report was queued.|
|**WerReportUploaded**<br/>2|The report was uploaded.|

## -returns

This function returns **S_OK** on success or an error code on failure.

## -remarks

After the application calls this function, WER collects the specified data. If the *consent* parameter is WerConsentApproved, it submits the report to Microsoft. If *consent* is WerConsentNotAsked, WER displays the consent dialog box. To determine the submission status, check the *pSubmitResult* parameter.

In the event of a critical application event, applications that have [registered for restart](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) will be restarted.

The computer identifier is sent with the report when:

- The consent used to send the report does not come from the application. For example, the report was submitted with consent status set to WerConsentNotAsked.
- The report was submitted with the WER_SUBMIT_REPORT_MACHINE_ID flag set.

To view the reports submitted by your application, go to Windows Quality Online Services.

## -see-also

[Application Recovery and Restart](/windows/desktop/wsw/portal), [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
