---
UID: NF:werapi.WerStoreOpen
title: WerStoreOpen function (werapi.h)
description: Opens the collection of stored error reports.
helpviewer_keywords: ["WerStoreOpen","WerStoreOpen function [Windows Error Reporting]","wer.werstoreopen","werapi/WerStoreOpen"]
old-location: wer\werstoreopen.htm
tech.root: wer
ms.assetid: FA7E0EC6-00F1-45E2-BE34-D732965FBA15
ms.date: 12/05/2018
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
 - wer.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerStoreOpen
---

# WerStoreOpen function


## -description

Opens the collection of stored error reports.

## -parameters

### -param repStoreType

The type of report store to open. See Remarks for details.

### -param phReportStore

A pointer to a report store. On a successful call, this will point to the retrieved report store.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not a valid value.

</td>
</tr>
</table>

## -remarks

A <i>storeType</i> value of <b>E_STORE_MACHINE_QUEUE</b> opens the queue of all error reports on the machine that have not yet been sent to Microsoft. A value of  <b>E_STORE_MACHINE_ARCHIVE</b> opens the store of error reports that have already been sent.

The Windows Error Report (WER) Store is the queue of error reports that have been marked to be sent to Microsoft but have not yet been uploaded. The upload of an error report can be postponed under a number of circumstances. The WerStore functions allow developers to access the stored reports and query the status of each one.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werstoreclose">WerStoreClose</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey">WerStoreGetFirstReportKey</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>