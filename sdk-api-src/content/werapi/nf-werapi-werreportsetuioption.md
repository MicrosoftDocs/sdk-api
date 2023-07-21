---
UID: NF:werapi.WerReportSetUIOption
title: WerReportSetUIOption function (werapi.h)
description: Sets the user interface options for the specified report.
helpviewer_keywords: ["WerReportSetUIOption","WerReportSetUIOption function [Windows Error Reporting]","WerUIAdditionalDataDlgHeader","WerUICloseDlgBody","WerUICloseDlgButtonText","WerUICloseDlgHeader","WerUICloseText","WerUIConsentDlgBody","WerUIConsentDlgHeader","WerUIIconFilePath","WerUIOfflineSolutionCheckText","WerUIOnlineSolutionCheckText","base.werreportsetuioption","wer.werreportsetuioption","werapi/WerReportSetUIOption"]
old-location: wer\werreportsetuioption.htm
tech.root: wer
ms.assetid: c8816782-faec-490e-898f-a40df8fb205b
ms.date: 12/05/2018
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

Sets the user interface options for the specified report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

### -param repUITypeID [in]

The user interface element to be customized. This parameter can be one of the following values from the **WER_REPORT_UI** enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerUIAdditionalDataDlgHeader"></a><a id="weruiadditionaldatadlgheader"></a><a id="WERUIADDITIONALDATADLGHEADER"></a><dl>
<dt>**WerUIAdditionalDataDlgHeader**</dt>
</dl>
</td>
<td width="60%">
The instructions for the additional data dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUICloseDlgBody"></a><a id="weruiclosedlgbody"></a><a id="WERUICLOSEDLGBODY"></a><dl>
<dt>**WerUICloseDlgBody**</dt>
</dl>
</td>
<td width="60%">
The contents of the close dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUICloseDlgButtonText"></a><a id="weruiclosedlgbuttontext"></a><a id="WERUICLOSEDLGBUTTONTEXT"></a><dl>
<dt>**WerUICloseDlgButtonText**</dt>
</dl>
</td>
<td width="60%">
The text for the button in the close dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUICloseDlgHeader"></a><a id="weruiclosedlgheader"></a><a id="WERUICLOSEDLGHEADER"></a><dl>
<dt>**WerUICloseDlgHeader**</dt>
</dl>
</td>
<td width="60%">
The main instructions for the close dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUICloseText"></a><a id="weruiclosetext"></a><a id="WERUICLOSETEXT"></a><dl>
<dt>**WerUICloseText**</dt>
</dl>
</td>
<td width="60%">
The text for the link to just terminate the application.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUIConsentDlgBody"></a><a id="weruiconsentdlgbody"></a><a id="WERUICONSENTDLGBODY"></a><dl>
<dt>**WerUIConsentDlgBody**</dt>
</dl>
</td>
<td width="60%">
The contents of the consent dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUIConsentDlgHeader"></a><a id="weruiconsentdlgheader"></a><a id="WERUICONSENTDLGHEADER"></a><dl>
<dt>**WerUIConsentDlgHeader**</dt>
</dl>
</td>
<td width="60%">
The main instructions for the consent dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUIIconFilePath"></a><a id="weruiiconfilepath"></a><a id="WERUIICONFILEPATH"></a><dl>
<dt>**WerUIIconFilePath**</dt>
</dl>
</td>
<td width="60%">
The icon to be displayed in the consent dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUIOfflineSolutionCheckText"></a><a id="weruiofflinesolutionchecktext"></a><a id="WERUIOFFLINESOLUTIONCHECKTEXT"></a><dl>
<dt>**WerUIOfflineSolutionCheckText**</dt>
</dl>
</td>
<td width="60%">
The text for the link to check for a solution when offline.

</td>
</tr>
<tr>
<td width="40%"><a id="WerUIOnlineSolutionCheckText"></a><a id="weruionlinesolutionchecktext"></a><a id="WERUIONLINESOLUTIONCHECKTEXT"></a><dl>
<dt>**WerUIOnlineSolutionCheckText**</dt>
</dl>
</td>
<td width="60%">
The text for the link to check for a solution when online.

</td>
</tr>
</table>

### -param pwzValue [in]

A pointer to a Unicode string that specifies the custom text. For more information, see the description of *repUITypeID*.

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also




<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



[Windows Error Reporting](/windows/desktop/wer)