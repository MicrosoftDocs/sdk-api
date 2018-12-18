---
UID: NF:werapi.WerFreeString
title: WerFreeString function
author: windows-sdk-content
description: Frees up the memory used to store a report key string. This should be called after each successive call to WerStoreGetFirstReportKey or WerStoreGetNextReportKey, once the particular report key string has been used and is no longer needed.
old-location: wer\werfreestring.htm
tech.root: wer
ms.assetid: 748AEFD4-3310-4BC1-A3DA-CFACBA31F2FC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WerFreeString, WerFreeString function [Windows Error Reporting], wer.werfreestring, werapi/WerFreeString
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
 - WerFreeString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerFreeString function


## -description


Frees up the memory used to store a report key string. This should be called after each successive call to <a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a> or <a href="https://msdn.microsoft.com/781D54A9-6F51-445E-89A8-A0C944081B81">WerStoreGetNextReportKey</a>, once the particular report key string has been used and is no longer needed.


## -parameters




### -param pwszStr

The string to be freed (value set to <b>NULL</b>).


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a>



<a href="https://msdn.microsoft.com/781D54A9-6F51-445E-89A8-A0C944081B81">WerStoreGetNextReportKey</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

