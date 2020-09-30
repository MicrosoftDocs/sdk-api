---
UID: NF:werapi.WerRegisterFile
title: WerRegisterFile function (werapi.h)
description: Registers a file to be collected when WER creates an error report.
helpviewer_keywords: ["WER_FILE_ANONYMOUS_DATA","WER_FILE_DELETE_WHEN_DONE","WerRegFileTypeMax","WerRegFileTypeOther","WerRegFileTypeUserDocument","WerRegisterFile","WerRegisterFile function [Windows Error Reporting]","base.werregisterfile","wer.werregisterfile","werapi/WerRegisterFile"]
old-location: wer\werregisterfile.htm
tech.root: wer
ms.assetid: 4b4bb1bb-6782-447a-901f-75702256d907
ms.date: 12/05/2018
ms.keywords: WER_FILE_ANONYMOUS_DATA, WER_FILE_DELETE_WHEN_DONE, WerRegFileTypeMax, WerRegFileTypeOther, WerRegFileTypeUserDocument, WerRegisterFile, WerRegisterFile function [Windows Error Reporting], base.werregisterfile, wer.werregisterfile, werapi/WerRegisterFile
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerRegisterFile
 - werapi/WerRegisterFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerRegisterFile
---

# WerRegisterFile function


## -description

Registers a file to be collected when WER creates an error report.

## -parameters

### -param pwzFile [in]

The full path to the file. The maximum length of this path is MAX_PATH characters.

### -param regFileType [in]

The file type. This parameter can be one of the following values from the <b>WER_REGISTER_FILE_TYPE</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerRegFileTypeMax"></a><a id="werregfiletypemax"></a><a id="WERREGFILETYPEMAX"></a><dl>
<dt><b>WerRegFileTypeMax</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The maximum value for the  <b>WER_REGISTER_FILE_TYPE</b> enumeration type.

</td>
</tr>
<tr>
<td width="40%"><a id="WerRegFileTypeOther"></a><a id="werregfiletypeother"></a><a id="WERREGFILETYPEOTHER"></a><dl>
<dt><b>WerRegFileTypeOther</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Any other type of file.

</td>
</tr>
<tr>
<td width="40%"><a id="WerRegFileTypeUserDocument"></a><a id="werregfiletypeuserdocument"></a><a id="WERREGFILETYPEUSERDOCUMENT"></a><dl>
<dt><b>WerRegFileTypeUserDocument</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The document in use by the application at the time of the event. This document is only collected if the Watson server asks for it.

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
<td width="40%"><a id="WER_FILE_ANONYMOUS_DATA"></a><a id="wer_file_anonymous_data"></a><dl>
<dt><b>WER_FILE_ANONYMOUS_DATA</b></dt>
</dl>
</td>
<td width="60%">
The file does not contain personal information that could be used to identify or contact the user.

</td>
</tr>
<tr>
<td width="40%"><a id="WER_FILE_DELETE_WHEN_DONE"></a><a id="wer_file_delete_when_done"></a><dl>
<dt><b>WER_FILE_DELETE_WHEN_DONE</b></dt>
</dl>
</td>
<td width="60%">
Automatically deletes the file after it is added to the report.

</td>
</tr>
</table>

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="/windows/desktop/wsw/portal">application recovery mode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The number of registered memory blocks and files exceeds the limit.

</td>
</tr>
</table>

## -remarks

The registered file is added to the report only when additional data is requested by the server.

For crashes and non-responses, the operating system automatically provides error reporting (you do not need to provide any error reporting code in your application). If you use this function to register a file, the operating system will add the file to the error report created at the time of a crash or non-response (this file is added in addition to the files the operating system already collects).


For generic event reporting, the application has to use the <a href="/windows/desktop/api/werapi/nf-werapi-werreportaddfile">WerReportAddFile</a> function instead. Alternatively, calling the <a href="/windows/desktop/api/werapi/nf-werapi-werreportsubmit">WerReportSubmit</a> function with the  WER_SUBMIT_ADD_REGISTERED_DATA flag will include the files that the <b>WerRegisterFile</b> function added.


To remove the file from the list, call the <a href="/windows/desktop/api/werapi/nf-werapi-werunregisterfile">WerUnregisterFile</a> function.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werunregisterfile">WerUnregisterFile</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>