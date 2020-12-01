---
UID: NF:werapi.WerReportCreate
title: WerReportCreate function (werapi.h)
description: Creates a problem report that describes an application event.
helpviewer_keywords: ["WerReportApplicationCrash","WerReportApplicationHang","WerReportCreate","WerReportCreate function [Windows Error Reporting]","WerReportCritical","WerReportInvalid","WerReportKernel","WerReportNonCritical","base.werreportcreate","wer.werreportcreate","werapi/WerReportCreate"]
old-location: wer\werreportcreate.htm
tech.root: wer
ms.assetid: 41f68dde-5e43-45a6-8e0b-3ae0c6180e8b
ms.date: 12/05/2018
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
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportCreate
---

# WerReportCreate function


## -description

Creates a problem report that describes an application event.

## -parameters

### -param pwzEventType [in]

A pointer to a Unicode string that specifies the name of the event.

### -param repType [in]

The type of report. This parameter can be one of the following values from the <b>WER_REPORT_TYPE</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerReportApplicationCrash"></a><a id="werreportapplicationcrash"></a><a id="WERREPORTAPPLICATIONCRASH"></a><dl>
<dt><b>WerReportApplicationCrash</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An error that has caused the application to stop running has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportApplicationHang"></a><a id="werreportapplicationhang"></a><a id="WERREPORTAPPLICATIONHANG"></a><dl>
<dt><b>WerReportApplicationHang</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
An error that has caused the application to stop responding has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportInvalid"></a><a id="werreportinvalid"></a><a id="WERREPORTINVALID"></a><dl>
<dt><b>WerReportInvalid</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
An error that has called out a return that is not valid has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportKernel"></a><a id="werreportkernel"></a><a id="WERREPORTKERNEL"></a><dl>
<dt><b>WerReportKernel</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
An error in the kernel has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportCritical"></a><a id="werreportcritical"></a><a id="WERREPORTCRITICAL"></a><dl>
<dt><b>WerReportCritical</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A critical error, such as a crash or non-response, has occurred. By default, processes that experience a critical error are terminated or restarted.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportNonCritical"></a><a id="werreportnoncritical"></a><a id="WERREPORTNONCRITICAL"></a><dl>
<dt><b>WerReportNonCritical</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An error that is not critical has occurred. This type of report shows no UI; the report is silently queued. It may then be sent silently to the server in the background if adequate user consent is available.

</td>
</tr>
</table>

### -param pReportInformation [in, optional]

A pointer to a <a href="/windows/desktop/api/werapi/ns-werapi-wer_report_information">WER_REPORT_INFORMATION</a> structure that specifies information for the report.

### -param phReportHandle [out]

A handle to the report. If the function fails, this handle is <b>NULL</b>.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure.

## -remarks

Use the following functions to specify additional information to be submitted:

<a href="/windows/desktop/api/werapi/nf-werapi-werreportadddump">WerReportAddDump</a>
<a href="/windows/desktop/api/werapi/nf-werapi-werreportaddfile">WerReportAddFile</a>
<a href="/windows/desktop/api/werapi/nf-werapi-werreportsetparameter">WerReportSetParameter</a>
To submit the information, call the <a href="/windows/desktop/api/werapi/nf-werapi-werreportsubmit">WerReportSubmit</a> function. When you have finished with the report handle, call the <a href="/windows/desktop/api/werapi/nf-werapi-werreportclosehandle">WerReportCloseHandle</a> function.

Applications can also indicate that they would like the opportunity to recover data or restart on failure. For more information, see <a href="/windows/desktop/wsw/portal">Application Recovery and Restart</a>.

To view the reports submitted by your application, go to Windows Quality Online Services.

## -see-also

<a href="/windows/desktop/wsw/portal">Application Recovery and Restart</a>



<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/ns-werapi-wer_report_information">WER_REPORT_INFORMATION</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werreportclosehandle">WerReportCloseHandle</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werreportsubmit">WerReportSubmit</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>