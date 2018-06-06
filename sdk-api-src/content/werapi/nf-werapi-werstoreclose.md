---
UID: NF:werapi.WerStoreClose
title: WerStoreClose function
author: windows-sdk-content
description: Closes the collection of stored reports.
old-location: wer\werstoreclose.htm
old-project: wer
ms.assetid: C34FBA67-5267-471C-B1AA-87BFC5725831
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: WerStoreClose, WerStoreClose function [Windows Error Reporting], wer.werstoreclose, werapi/WerStoreClose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
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
product: Windows
targetos: Windows
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerStoreClose function


## -description


Closes the collection of stored reports.


## -parameters




### -param hReportStore

TBD




#### - store

The error report store to close (previously retrieved with <a href="https://msdn.microsoft.com/FA7E0EC6-00F1-45E2-BE34-D732965FBA15">WerStoreOpen</a>).


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/FA7E0EC6-00F1-45E2-BE34-D732965FBA15">WerStoreOpen</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

