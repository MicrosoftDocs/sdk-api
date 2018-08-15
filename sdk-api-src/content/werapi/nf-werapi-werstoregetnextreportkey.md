---
UID: NF:werapi.WerStoreGetNextReportKey
title: WerStoreGetNextReportKey function
author: windows-sdk-content
description: Gets a reference to the next report in the error report store.
old-location: wer\werstoregetnextreportkey.htm
old-project: wer
ms.assetid: 781D54A9-6F51-445E-89A8-A0C944081B81
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WerStoreGetNextReportKey, WerStoreGetNextReportKey function [Windows Error Reporting], wer.werstoregetnextreportkey, werapi/WerStoreGetNextReportKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: werapi.h
req.include-header: 
req.redist: 
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
 - WerStoreGetNextReportKey
product: Windows
targetos: Windows
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerStoreGetNextReportKey function


## -description


Gets a reference to the next report in the error report store.


## -parameters




### -param hReportStore

The error report store (previously retrieved with <a href="https://msdn.microsoft.com/FA7E0EC6-00F1-45E2-BE34-D732965FBA15">WerStoreOpen</a>).


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




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

