---
UID: NF:werapi.WerStoreGetFirstReportKey
title: WerStoreGetFirstReportKey function (werapi.h)
description: Gets a reference to the first report in the report store.
helpviewer_keywords: ["WerStoreGetFirstReportKey","WerStoreGetFirstReportKey function [Windows Error Reporting]","wer.werstoregetfirstreportkey","werapi/WerStoreGetFirstReportKey"]
old-location: wer\werstoregetfirstreportkey.htm
tech.root: wer
ms.assetid: E4732B60-BFBE-4916-83A6-5F031D267913
ms.date: 12/05/2018
ms.keywords: WerStoreGetFirstReportKey, WerStoreGetFirstReportKey function [Windows Error Reporting], wer.werstoregetfirstreportkey, werapi/WerStoreGetFirstReportKey
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
 - WerStoreGetFirstReportKey
 - werapi/WerStoreGetFirstReportKey
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
 - WerStoreGetFirstReportKey
---

# WerStoreGetFirstReportKey function


## -description

Gets a reference to the first report in the report store.

## -parameters

### -param hReportStore

The error report store (previously retrieved with <a href="/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>).

### -param ppszReportKey

A pointer to the report key string. On a successful call, this will point to the retrieved report key.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**E_INVALID_ARG**</dt>
</dl>
</td>
<td width="60%">
One of the arguments is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**ERROR_NO_MORE_FILES**</dt>
</dl>
</td>
<td width="60%">
There are no error reports in the store.

</td>
</tr>
</table>

## -see-also




{WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey)



<a href="/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>



[Windows Error Reporting](/windows/desktop/wer)