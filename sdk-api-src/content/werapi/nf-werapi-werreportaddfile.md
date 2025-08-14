---
UID: NF:werapi.WerReportAddFile
title: WerReportAddFile function (werapi.h)
description: Adds a file to the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WER_FILE_ANONYMOUS_DATA","WER_FILE_DELETE_WHEN_DONE","WerFileTypeHeapdump","WerFileTypeMicrodump","WerFileTypeMinidump","WerFileTypeOther","WerFileTypeUserDocument","WerReportAddFile","WerReportAddFile function [Windows Error Reporting]","base.werreportaddfile","wer.werreportaddfile","werapi/WerReportAddFile"]
old-location: wer\werreportaddfile.htm
tech.root: wer
ms.assetid: 4b2c2060-a193-4168-90fc-afb95c160569
ms.date: 07/25/2023
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
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportAddFile
---

# WerReportAddFile function

## -description

Adds a file to the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

### -param pwzPath [in]

A pointer to a Unicode string that contains the full path to the file to be added. This path can use environment variables. The maximum length of this path is MAX_PATH characters.

### -param repFileType [in]

The type of file. This parameter can be one of the following values from the **WER_FILE_TYPE** enumeration type.

|Value|Meaning|
|--- |--- |
|**WerFileTypeHeapdump**|An extended minidump that contains additional data such as the process memory.|
|**WerFileTypeMicrodump**|A limited minidump that contains only a stack trace.|
|**WerFileTypeMinidump**|A minidump file.|
|**WerFileTypeOther**|Any other type of file. This file will always get added to the cab (but only if the server asks for a cab).|
|**WerFileTypeUserDocument**|The document in use by the application at the time of the event. The document is added only if the server is asks for this type of document.|

### -param dwFileFlags [in]

This parameter can be one or more of the following values.

|Value|Meaning|
|--- |--- |
|**WER_FILE_ANONYMOUS_DATA**|The file does not contain personal information that could be used to identify or contact the user.|
|**WER_FILE_DELETE_WHEN_DONE**|Automatically delete the file after the report is submitted.|

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)**|The specified file does not exist.|
|**HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)**|The specified file is a user-document and is stored on an encrypted file-system; this combination is not supported.|

## -remarks

Although this function can also be used to add memory dumps (using specific flags) to the error report, the preferred function to use for adding memory dumps is [WerReportAddDump](/windows/desktop/api/werapi/nf-werapi-werreportadddump). You should use this function only if you want to collect the dump yourself and then add it to the report.

## -see-also

[WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
