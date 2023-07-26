---
UID: NF:werapi.WerFreeString
title: WerFreeString function (werapi.h)
description: Frees up the memory used to store a report key string. This should be called after each successive call to WerStoreGetFirstReportKey or WerStoreGetNextReportKey, once the particular report key string has been used and is no longer needed.
helpviewer_keywords: ["WerFreeString","WerFreeString function [Windows Error Reporting]","wer.werfreestring","werapi/WerFreeString"]
old-location: wer\werfreestring.htm
tech.root: wer
ms.assetid: 748AEFD4-3310-4BC1-A3DA-CFACBA31F2FC
ms.date: 07/25/2023
ms.keywords: WerFreeString, WerFreeString function [Windows Error Reporting], wer.werfreestring, werapi/WerFreeString
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
 - WerFreeString
 - werapi/WerFreeString
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
 - WerFreeString
---

# WerFreeString function

## -description

Frees up the memory used to store a [Windows Error Reporting](../_wer/index.md) (WER) key string.

## -parameters

### -param pwszStr

The string to be freed (value set to **NULL**).

### -remarks

This method should be called after each successive call to [WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey) or [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey), once the particular report key string has been used and is no longer needed.

## -see-also

[WerStoreGetFirstReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetfirstreportkey), [WerStoreGetNextReportKey](/windows/desktop/api/werapi/nf-werapi-werstoregetnextreportkey), [Windows Error Reporting](/windows/desktop/wer)
