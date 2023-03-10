---
UID: NF:werapi.WerStoreGetNextReportKey
title: WerStoreGetNextReportKey function (werapi.h)
description: Gets a reference to the next report in the error report store.
helpviewer_keywords: ["WerStoreGetNextReportKey","WerStoreGetNextReportKey function [Windows Error Reporting]","wer.werstoregetnextreportkey","werapi/WerStoreGetNextReportKey"]
old-location: wer\werstoregetnextreportkey.htm
tech.root: wer
ms.assetid: 781D54A9-6F51-445E-89A8-A0C944081B81
ms.date: 12/05/2018
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
 - wer.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerStoreGetNextReportKey
---

# WerStoreGetNextReportKey function


## -description

Gets a reference to the next report in the error report store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with <a href="/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>).

### -param ppszReportKey

A pointer to the report key string. On a successful call, this will point to the retrieved report key.

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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_FILES</b></dt>
</dl>
</td>
<td width="60%">
There are no more error reports in the store.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey">WerStoreGetFirstReportKey</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>