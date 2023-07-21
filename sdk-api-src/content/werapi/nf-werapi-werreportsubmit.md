---
UID: NF:werapi.WerReportSubmit
title: WerReportSubmit function (werapi.h)
description: Submits the specified report.
helpviewer_keywords: ["WER_SUBMIT_ADD_REGISTERED_DATA","WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY","WER_SUBMIT_BYPASS_DATA_THROTTLING","WER_SUBMIT_HONOR_RECOVERY","WER_SUBMIT_HONOR_RESTART","WER_SUBMIT_NO_ARCHIVE","WER_SUBMIT_NO_CLOSE_UI","WER_SUBMIT_NO_QUEUE","WER_SUBMIT_OUTOFPROCESS","WER_SUBMIT_OUTOFPROCESS_ASYNC","WER_SUBMIT_QUEUE","WER_SUBMIT_REPORT_MACHINE_ID","WER_SUBMIT_SHOW_DEBUG","WER_SUBMIT_START_MINIMIZED","WerConsentAlwaysPrompt","WerConsentApproved","WerConsentDenied","WerConsentMax","WerConsentNotAsked","WerCustomAction","WerDisabled","WerDisabledQueue","WerReportAsync","WerReportCancelled","WerReportDebug","WerReportFailed","WerReportQueued","WerReportSubmit","WerReportSubmit function [Windows Error Reporting]","WerReportUploaded","base.werreportsubmit","wer.werreportsubmit","werapi/WerReportSubmit"]
old-location: wer\werreportsubmit.htm
tech.root: wer
ms.assetid: 1433862e-5cf6-4d31-9fd9-137b7b86ec57
ms.date: 12/05/2018
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
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportSubmit
---

# WerReportSubmit function


## -description

Submits the specified report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

### -param consent [in]

The consent status. This parameter can be one of the following values from the [**WER_CONSENT**](ne-werapi-wer_consent.md) enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerConsentAlwaysPrompt"></a><a id="werconsentalwaysprompt"></a><a id="WERCONSENTALWAYSPROMPT"></a><dl>
<dt>**WerConsentAlwaysPrompt**</dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The user is always asked to submit the request.

</td>
</tr>
<tr>
<td width="40%"><a id="WerConsentApproved"></a><a id="werconsentapproved"></a><a id="WERCONSENTAPPROVED"></a><dl>
<dt>**WerConsentApproved**</dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The user has approved the submission request.

</td>
</tr>
<tr>
<td width="40%"><a id="WerConsentDenied"></a><a id="werconsentdenied"></a><a id="WERCONSENTDENIED"></a><dl>
<dt>**WerConsentDenied**</dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The user has denied the submission request.

</td>
</tr>
<tr>
<td width="40%"><a id="WerConsentMax"></a><a id="werconsentmax"></a><a id="WERCONSENTMAX"></a><dl>
<dt>**WerConsentMax**</dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The maximum value for the **WER_CONSENT** enumeration type.

</td>
</tr>
<tr>
<td width="40%"><a id="WerConsentNotAsked"></a><a id="werconsentnotasked"></a><a id="WERCONSENTNOTASKED"></a><dl>
<dt>**WerConsentNotAsked**</dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The user was not asked for consent.

</td>
</tr>
</table>

### -param dwFlags [in]

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_ADD_REGISTERED_DATA"></a><a id="wer_submit_add_registered_data"></a><dl>
<dt>**WER_SUBMIT_ADD_REGISTERED_DATA**</dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Add the data registered by [WerSetFlags](/windows/desktop/api/werapi/nf-werapi-wersetflags), <a href="/windows/desktop/api/werapi/nf-werapi-werregisterfile">WerRegisterFile</a>, and <a href="/windows/desktop/api/werapi/nf-werapi-werregistermemoryblock">WerRegisterMemoryBlock</a> to the report.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_HONOR_RECOVERY"></a><a id="wer_submit_honor_recovery"></a><dl>
<dt>**WER_SUBMIT_HONOR_RECOVERY**</dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Honor any recovery registration for the application. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrecoverycallback">RegisterApplicationRecoveryCallback</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_HONOR_RESTART"></a><a id="wer_submit_honor_restart"></a><dl>
<dt>**WER_SUBMIT_HONOR_RESTART**</dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Honor any restart registration for the application. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_NO_ARCHIVE"></a><a id="wer_submit_no_archive"></a><dl>
<dt>**WER_SUBMIT_NO_ARCHIVE**</dt>
<dt>256</dt>
</dl>
</td>
<td width="60%">
Do not archive the report.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_NO_CLOSE_UI"></a><a id="wer_submit_no_close_ui"></a><dl>
<dt>**WER_SUBMIT_NO_CLOSE_UI**</dt>
<dt>64</dt>
</dl>
</td>
<td width="60%">
Do not display the close dialog box for the critical report.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_NO_QUEUE"></a><a id="wer_submit_no_queue"></a><dl>
<dt>**WER_SUBMIT_NO_QUEUE**</dt>
<dt>128</dt>
</dl>
</td>
<td width="60%">
Do not queue the report. If there is adequate user consent the report is sent to Microsoft immediately; otherwise, the report is discarded. You may use this flag for non-critical reports. 

The report is discarded for any action that would require the report to be queued. For example, if the computer is offline when you submit the report, the report is discarded. Also, if there is insufficient consent (for example, consent was required for the data portion of the report), the report is discarded.


</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_OUTOFPROCESS"></a><a id="wer_submit_outofprocess"></a><dl>
<dt>**WER_SUBMIT_OUTOFPROCESS**</dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
Spawn another process to submit the report. The calling thread is blocked until the function returns.

> [!NOTE]
> Window messages will be pumped so that UI activity on the calling thread is not blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_OUTOFPROCESS_ASYNC"></a><a id="wer_submit_outofprocess_async"></a><dl>
<dt>**WER_SUBMIT_OUTOFPROCESS_ASYNC**</dt>
<dt>1024</dt>
</dl>
</td>
<td width="60%">
Spawn another process to submit the report and return from this function call immediately. Note that the contents of the *pSubmitResult* parameter are undefined and there is no way to query when the reporting completes or the completion status.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_QUEUE"></a><a id="wer_submit_queue"></a><dl>
<dt>**WER_SUBMIT_QUEUE**</dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Add the report to the WER queue without notifying the user.  The report is queued only—reporting (sending the report to Microsoft) occurs later based on the user's consent level.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_SHOW_DEBUG"></a><a id="wer_submit_show_debug"></a><dl>
<dt>**WER_SUBMIT_SHOW_DEBUG**</dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Show the debug button.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_START_MINIMIZED"></a><a id="wer_submit_start_minimized"></a><dl>
<dt>**WER_SUBMIT_START_MINIMIZED**</dt>
<dt>512</dt>
</dl>
</td>
<td width="60%">
The initial UI is minimized and flashing.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_BYPASS_DATA_THROTTLING"></a><a id="wer_submit_bypass_data_throttling"></a><dl>
<dt>**WER_SUBMIT_BYPASS_DATA_THROTTLING**</dt>
<dt>2048</dt>
</dl>
</td>
<td width="60%">
Bypass data throttling for the report.

**Windows 7 or earlier:  **This parameter is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY"></a><a id="wer_submit_archive_parameters_only"></a><dl>
<dt>**WER_SUBMIT_ARCHIVE_PARAMETERS_ONLY**</dt>
<dt>4096</dt>
</dl>
</td>
<td width="60%">
Archive only the parameters; the cab is discarded. This flag overrides the <a href="/windows/desktop/wer/wer-settings">ConfigureArchive</a> WER setting.

**Windows 7 or earlier:  **This parameter is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_SUBMIT_REPORT_MACHINE_ID"></a><a id="wer_submit_report_machine_id"></a><dl>
<dt>**WER_SUBMIT_REPORT_MACHINE_ID**</dt>
<dt>8192</dt>
</dl>
</td>
<td width="60%">
Always send the unique, 128-bit computer identifier with the report, regardless of the consent with which the report was submitted. See Remarks for additional information.

**Windows 7 or earlier:  **This parameter is not available.

</td>
</tr>
</table>

### -param pSubmitResult [out, optional]

The result of the submission. This parameter can be one of the following values from the **WER_SUBMIT_RESULT** enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerCustomAction"></a><a id="wercustomaction"></a><a id="WERCUSTOMACTION"></a><dl>
<dt>**WerCustomAction**</dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Error reporting can be customized.

</td>
</tr>
<tr>
<td width="40%"><a id="WerDisabled"></a><a id="werdisabled"></a><a id="WERDISABLED"></a><dl>
<dt>**WerDisabled**</dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Error reporting was disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="WerDisabledQueue"></a><a id="werdisabledqueue"></a><a id="WERDISABLEDQUEUE"></a><dl>
<dt>**WerDisabledQueue**</dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Queuing was disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportAsync"></a><a id="werreportasync"></a><a id="WERREPORTASYNC"></a><dl>
<dt>**WerReportAsync**</dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The report was asynchronous.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportCancelled"></a><a id="werreportcancelled"></a><a id="WERREPORTCANCELLED"></a><dl>
<dt>**WerReportCancelled**</dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The report was canceled.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportDebug"></a><a id="werreportdebug"></a><a id="WERREPORTDEBUG"></a><dl>
<dt>**WerReportDebug**</dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The Debug button was clicked.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportFailed"></a><a id="werreportfailed"></a><a id="WERREPORTFAILED"></a><dl>
<dt>**WerReportFailed**</dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The report submission failed.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportQueued"></a><a id="werreportqueued"></a><a id="WERREPORTQUEUED"></a><dl>
<dt>**WerReportQueued**</dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The report was queued.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportUploaded"></a><a id="werreportuploaded"></a><a id="WERREPORTUPLOADED"></a><dl>
<dt>**WerReportUploaded**</dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The report was uploaded.

</td>
</tr>
</table>

## -returns

This function returns **S_OK** on success or an error code on failure.

## -remarks

After the application calls this function, WER collects the specified data. If the *consent* parameter is WerConsentApproved, it submits the report to Microsoft. If *consent* is WerConsentNotAsked, WER displays the consent dialog box. To determine the submission status, check the *pSubmitResult* parameter.

In the event of a critical application event, applications that have <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">registered for restart</a> will be restarted.

The computer identifier is sent with the report when

<ul>
<li>The consent used to send the report does not come from the application. For example, the report was submitted with consent status set to WerConsentNotAsked.</li>
<li>The report was submitted with the WER_SUBMIT_REPORT_MACHINE_ID flag set.</li>
</ul>
To view the reports submitted by your application, go to Windows Quality Online Services.

## -see-also

<a href="/windows/desktop/wsw/portal">Application Recovery and Restart</a>






<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



[Windows Error Reporting](/windows/desktop/wer)
