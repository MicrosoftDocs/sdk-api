---
UID: NF:werapi.WerReportCloseHandle
title: WerReportCloseHandle function
author: windows-sdk-content
description: Closes the specified report.
old-location: wer\werreportclosehandle.htm
tech.root: wer
ms.assetid: b7326003-cd25-4988-9ed4-31c2e030beec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WerReportCloseHandle, WerReportCloseHandle function [Windows Error Reporting], base.werreportclosehandle, wer.werreportclosehandle, werapi/WerReportCloseHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportCloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerReportCloseHandle function


## -description


Closes the specified report.


## -parameters




### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a> function.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

