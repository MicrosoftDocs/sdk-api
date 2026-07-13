---
UID: NF:werapi.WerReportCloseHandle
title: WerReportCloseHandle function (werapi.h)
description: Closes the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WerReportCloseHandle","WerReportCloseHandle function [Windows Error Reporting]","base.werreportclosehandle","wer.werreportclosehandle","werapi/WerReportCloseHandle"]
old-location: wer\werreportclosehandle.htm
tech.root: wer
ms.assetid: b7326003-cd25-4988-9ed4-31c2e030beec
ms.date: 07/25/2023
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
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportCloseHandle
---

# WerReportCloseHandle function

## -description

Closes the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also

[WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
