---
UID: NF:werapi.WerStoreOpen
title: WerStoreOpen function (werapi.h)
description: Opens the collection of stored Windows Error Reporting (WER) error reports.
helpviewer_keywords: ["WerStoreOpen","WerStoreOpen function [Windows Error Reporting]","wer.werstoreopen","werapi/WerStoreOpen"]
old-location: wer\werstoreopen.htm
tech.root: wer
ms.assetid: FA7E0EC6-00F1-45E2-BE34-D732965FBA15
ms.date: 07/26/2023
ms.keywords: WerStoreOpen, WerStoreOpen function [Windows Error Reporting], wer.werstoreopen, werapi/WerStoreOpen
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
 - WerStoreOpen
 - werapi/WerStoreOpen
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
 - WerStoreOpen
---

# WerStoreOpen function

## -description

Opens the collection of stored [Windows Error Reporting](../_wer/index.md) (WER) error reports.

## -parameters

### -param repStoreType

The type of report store to open. See Remarks for details.

### -param phReportStore

A pointer to a report store. On a successful call, this will point to the retrieved report store.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**E_INVALIDARG**|One of the arguments is not a valid value.|

## -remarks

A *storeType* value of **E_STORE_MACHINE_QUEUE** opens the queue of all error reports on the machine that have not yet been sent to Microsoft. A value of  **E_STORE_MACHINE_ARCHIVE** opens the store of error reports that have already been sent.

The Windows Error Report (WER) Store is the queue of error reports that have been marked to be sent to Microsoft but have not yet been uploaded. The upload of an error report can be postponed under a number of circumstances. The WerStore functions allow developers to access the stored reports and query the status of each one.

## -see-also

[WerStoreClose](/windows/desktop/api/werapi/nf-werapi-werstoreclose), [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey), [Windows Error Reporting](/windows/desktop/wer)
