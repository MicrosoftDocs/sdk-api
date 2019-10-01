---
UID: NF:werapi.WerStoreClose
title: WerStoreClose function (werapi.h)
author: windows-sdk-content
description: Closes the collection of stored reports.
old-location: wer\werstoreclose.htm
tech.root: wer
ms.assetid: C34FBA67-5267-471C-B1AA-87BFC5725831
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WerStoreClose, WerStoreClose function [Windows Error Reporting], wer.werstoreclose, werapi/WerStoreClose
ms.topic: function
f1_keywords: 
 - "werapi/WerStoreClose"
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
 - WerStoreClose
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WerStoreClose function


## -description


Closes the collection of stored reports.


## -parameters




### -param hReportStore

The error report store to close (previously retrieved with <a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>).


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werstoreopen">WerStoreOpen</a>



<a href="https://docs.microsoft.com/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>
 

 

