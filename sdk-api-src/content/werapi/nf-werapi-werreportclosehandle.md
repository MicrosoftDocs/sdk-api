---
UID: NF:werapi.WerReportCloseHandle
title: WerReportCloseHandle function (werapi.h)
description: Closes the specified report.
helpviewer_keywords: ["WerReportCloseHandle","WerReportCloseHandle function [Windows Error Reporting]","base.werreportclosehandle","wer.werreportclosehandle","werapi/WerReportCloseHandle"]
old-location: wer\werreportclosehandle.htm
tech.root: wer
ms.assetid: b7326003-cd25-4988-9ed4-31c2e030beec
ms.date: 12/05/2018
ms.keywords: WerReportCloseHandle, WerReportCloseHandle function [Windows Error Reporting], base.werreportclosehandle, wer.werreportclosehandle, werapi/WerReportCloseHandle
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
 - WerReportCloseHandle
 - werapi/WerReportCloseHandle
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
 - WerReportCloseHandle
---

# WerReportCloseHandle function


## -description

Closes the specified report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>