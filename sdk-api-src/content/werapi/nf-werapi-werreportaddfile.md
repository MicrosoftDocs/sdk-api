---
UID: NF:werapi.WerReportAddFile
title: WerReportAddFile function (werapi.h)
description: Adds a file to the specified report.
helpviewer_keywords: ["WER_FILE_ANONYMOUS_DATA","WER_FILE_DELETE_WHEN_DONE","WerFileTypeHeapdump","WerFileTypeMicrodump","WerFileTypeMinidump","WerFileTypeOther","WerFileTypeUserDocument","WerReportAddFile","WerReportAddFile function [Windows Error Reporting]","base.werreportaddfile","wer.werreportaddfile","werapi/WerReportAddFile"]
old-location: wer\werreportaddfile.htm
tech.root: wer
ms.assetid: 4b2c2060-a193-4168-90fc-afb95c160569
ms.date: 12/05/2018
ms.keywords: WER_FILE_ANONYMOUS_DATA, WER_FILE_DELETE_WHEN_DONE, WerFileTypeHeapdump, WerFileTypeMicrodump, WerFileTypeMinidump, WerFileTypeOther, WerFileTypeUserDocument, WerReportAddFile, WerReportAddFile function [Windows Error Reporting], base.werreportaddfile, wer.werreportaddfile, werapi/WerReportAddFile
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
 - WerReportAddFile
 - werapi/WerReportAddFile
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
 - WerReportAddFile
---

# WerReportAddFile function


## -description

Adds a file to the specified  report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

### -param pwzPath [in]

A pointer to a Unicode string that contains the full path to the file to be added. This path can use environment variables. The maximum length of this path is MAX_PATH characters.

### -param repFileType [in]

The type of file. This parameter can be one of the following values from the **WER_FILE_TYPE** enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerFileTypeHeapdump"></a><a id="werfiletypeheapdump"></a><a id="WERFILETYPEHEAPDUMP"></a><dl>
<dt>**WerFileTypeHeapdump**</dt>
</dl>
</td>
<td width="60%">
An extended minidump that contains additional data such as the process memory.

</td>
</tr>
<tr>
<td width="40%"><a id="WerFileTypeMicrodump"></a><a id="werfiletypemicrodump"></a><a id="WERFILETYPEMICRODUMP"></a><dl>
<dt>**WerFileTypeMicrodump**</dt>
</dl>
</td>
<td width="60%">
A limited minidump that contains only a stack trace.

</td>
</tr>
<tr>
<td width="40%"><a id="WerFileTypeMinidump"></a><a id="werfiletypeminidump"></a><a id="WERFILETYPEMINIDUMP"></a><dl>
<dt>**WerFileTypeMinidump**</dt>
</dl>
</td>
<td width="60%">
A minidump file.

</td>
</tr>
<tr>
<td width="40%"><a id="WerFileTypeOther"></a><a id="werfiletypeother"></a><a id="WERFILETYPEOTHER"></a><dl>
<dt>**WerFileTypeOther**</dt>
</dl>
</td>
<td width="60%">
Any other type of file. This file will always get added to the cab (but only if the server asks for a cab).

</td>
</tr>
<tr>
<td width="40%"><a id="WerFileTypeUserDocument"></a><a id="werfiletypeuserdocument"></a><a id="WERFILETYPEUSERDOCUMENT"></a><dl>
<dt>**WerFileTypeUserDocument**</dt>
</dl>
</td>
<td width="60%">
The document in use by the application at the time of the event. The document is added only if the server is asks for this type of document.

</td>
</tr>
</table>

### -param dwFileFlags [in]

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WER_FILE_ANONYMOUS_DATA"></a><a id="wer_file_anonymous_data"></a><dl>
<dt>**WER_FILE_ANONYMOUS_DATA**</dt>
</dl>
</td>
<td width="60%">
The file does not contain personal information that could be used to identify or contact the user.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FILE_DELETE_WHEN_DONE"></a><a id="wer_file_delete_when_done"></a><dl>
<dt>**WER_FILE_DELETE_WHEN_DONE**</dt>
</dl>
</td>
<td width="60%">
Automatically delete the file after the report is submitted.

</td>
</tr>
</table>

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)**</dt>
</dl>
</td>
<td width="60%">
The specified file does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)**</dt>
</dl>
</td>
<td width="60%">
The specified file is a user-document and is stored on an encrypted file-system; this combination is not supported.

</td>
</tr>
</table>

## -remarks

Although this function can also be used to add memory dumps (using specific flags) to the error report, the preferred function to use for adding memory dumps is <a href="/windows/desktop/api/werapi/nf-werapi-werreportadddump">WerReportAddDump</a>. You should use this function only if you want to collect the dump yourself and then add it to the report.

## -see-also




<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



[Windows Error Reporting](/windows/desktop/wer)