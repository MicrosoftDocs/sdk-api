---
UID: NF:werapi.WerStoreGetNextReportKey
title: WerStoreGetNextReportKey function (werapi.h)
description: Gets a reference to the next Windows Error Reporting (WER) report in the error report store.
helpviewer_keywords: ["WerStoreGetNextReportKey","WerStoreGetNextReportKey function [Windows Error Reporting]","wer.werstoregetnextreportkey","werapi/WerStoreGetNextReportKey"]
old-location: wer\werstoregetnextreportkey.htm
tech.root: wer
ms.assetid: 781D54A9-6F51-445E-89A8-A0C944081B81
ms.date: 07/26/2023
ms.keywords: WerStoreGetNextReportKey, WerStoreGetNextReportKey function [Windows Error Reporting], wer.werstoregetnextreportkey, werapi/WerStoreGetNextReportKey
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
 - WerStoreGetNextReportKey
 - werapi/WerStoreGetNextReportKey
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
 - WerStoreGetNextReportKey
---

# WerStoreGetNextReportKey function

## -description

Gets a reference to the next [Windows Error Reporting](../_wer/index.md) (WER) report in the error report store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with [WerStoreOpen](/windows/desktop/api/werapi/nf-werapi-werstoreopen)).

### -param ppszReportKey

A pointer to the report key string. On a successful call, this will point to the retrieved report key.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**E_INVALID_ARG**|One of the arguments is not a valid value.|
|**ERROR_NO_MORE_FILES**|There are no more error reports in the store.|

## -see-also

[WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey), [Windows Error Reporting](/windows/desktop/wer)
