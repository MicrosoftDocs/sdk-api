---
UID: NF:werapi.WerStoreUploadReport
tech.root: wer
title: WerStoreUploadReport
ms.date: 07/21/2023
targetos: Windows
description: Uploads a report to the Windows Error Reporting (WER) store.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: werapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - ext-ms-win-wer-reporting-l1-1-1.dll
 - werapi.h
api_name:
 - WerStoreUploadReport
f1_keywords:
 - WerStoreUploadReport
 - werapi/WerStoreUploadReport
dev_langs:
 - c++
helpviewer_keywords:
 - WerStoreUploadReport
---

# WerStoreUploadReport function

## -description

Uploads a report to the [Windows Error Reporting](../_wer/index.md) (WER) store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

### -param pszReportKey

The string identifying which report is being queried (previously retrieved with [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey) or [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey)).

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

## -see-also

[Windows Error Reporting](../_wer/index.md)
