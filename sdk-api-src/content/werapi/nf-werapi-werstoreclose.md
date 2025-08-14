---
UID: NF:werapi.WerStoreClose
title: WerStoreClose function (werapi.h)
description: Closes the collection of stored Windows Error Reporting (WER) reports.
helpviewer_keywords: ["WerStoreClose","WerStoreClose function [Windows Error Reporting]","wer.werstoreclose","werapi/WerStoreClose"]
old-location: wer\werstoreclose.htm
tech.root: wer
ms.assetid: C34FBA67-5267-471C-B1AA-87BFC5725831
ms.date: 07/26/2023
ms.keywords: WerStoreClose, WerStoreClose function [Windows Error Reporting], wer.werstoreclose, werapi/WerStoreClose
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - WerStoreClose
 - werapi/WerStoreClose
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
 - ext-ms-win-wer-reporting-l1-1-1.dll
 - wer.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerStoreClose
---

# WerStoreClose function

## -description

Closes the collection of stored [Windows Error Reporting](../_wer/index.md) (WER) reports.

## -parameters

### -param hReportStore

The error report store to close (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

## -returns

This function returns **S_OK** on success or an error code on failure.

## -see-also

[WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen), [Windows Error Reporting](/windows/desktop/wer)
