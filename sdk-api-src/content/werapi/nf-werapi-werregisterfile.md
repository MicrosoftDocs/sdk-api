---
UID: NF:werapi.WerRegisterFile
title: WerRegisterFile function (werapi.h)
description: Registers a file to be collected when Windows Error Reporting (WER) creates an error report.
helpviewer_keywords: ["WER_FILE_ANONYMOUS_DATA","WER_FILE_DELETE_WHEN_DONE","WerRegFileTypeMax","WerRegFileTypeOther","WerRegFileTypeUserDocument","WerRegisterFile","WerRegisterFile function [Windows Error Reporting]","base.werregisterfile","wer.werregisterfile","werapi/WerRegisterFile"]
old-location: wer\werregisterfile.htm
tech.root: wer
ms.assetid: 4b4bb1bb-6782-447a-901f-75702256d907
ms.date: 07/25/2023
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
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - api-ms-win-core-windowserrorreporting-l1-1-2.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerRegisterFile
---

# WerRegisterFile function

## -description

Registers a file to be collected when [Windows Error Reporting](../_wer/index.md) (WER) creates an error report.

## -parameters

### -param pwzFile [in]

The full path to the file. The maximum length of this path is MAX_PATH characters.

### -param regFileType [in]

The file type. This parameter can be one of the following values from the **WER_REGISTER_FILE_TYPE** enumeration type.

|Value|Meaning|
|--- |--- |
|**WerRegFileTypeMax**
3|The maximum value for the  **WER_REGISTER_FILE_TYPE** enumeration type.|
|**WerRegFileTypeOther**
2|Any other type of file.|
|**WerRegFileTypeUserDocument**
1|The document in use by the application at the time of the event. This document is only collected if the Watson server asks for it.|

### -param dwFlags [in]

This parameter can be one or more of the following values.

|Value|Meaning|
|--- |--- |
|**WER_FILE_ANONYMOUS_DATA**|The file does not contain personal information that could be used to identify or contact the user.|
|**WER_FILE_DELETE_WHEN_DONE**|Automatically deletes the file after it is added to the report.|

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|
|**HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)**|The number of registered memory blocks and files exceeds the limit.|

## -remarks

The registered file is added to the report only when additional data is requested by the server.

For crashes and non-responses, the operating system automatically provides error reporting (you do not need to provide any error reporting code in your application). If you use this function to register a file, the operating system will add the file to the error report created at the time of a crash or non-response (this file is added in addition to the files the operating system already collects).

For generic event reporting, the application has to use the [WerReportAddFile](/windows/desktop/api/werapi/nf-werapi-werreportaddfile) function instead. Alternatively, calling the [WerReportSubmit](/windows/desktop/api/werapi/nf-werapi-werreportsubmit) function with the  WER_SUBMIT_ADD_REGISTERED_DATA flag will include the files that the **WerRegisterFile** function added.

To remove the file from the list, call the [WerUnregisterFile](/windows/desktop/api/werapi/nf-werapi-werunregisterfile) function.

## -see-also

[WerUnregisterFile](/windows/desktop/api/werapi/nf-werapi-werunregisterfile), [Windows Error Reporting](/windows/desktop/wer)
