---
UID: NS:werapi._WER_EXCEPTION_INFORMATION
title: WER_EXCEPTION_INFORMATION (werapi.h)
author: windows-sdk-content
description: Contains exception information for the WerReportAddDump function.
old-location: wer\wer_exception_information.htm
tech.root: wer
ms.assetid: 4548068a-e654-40c9-9654-c5178575b42c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWER_EXCEPTION_INFORMATION, PWER_EXCEPTION_INFORMATION, PWER_EXCEPTION_INFORMATION structure pointer [Windows Error Reporting], WER_EXCEPTION_INFORMATION, WER_EXCEPTION_INFORMATION structure [Windows Error Reporting], base.wer_exception_information, wer.wer_exception_information, werapi/PWER_EXCEPTION_INFORMATION, werapi/WER_EXCEPTION_INFORMATION"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Werapi.h
api_name:
 - WER_EXCEPTION_INFORMATION
product: Windows
targetos: Windows
req.typenames: WER_EXCEPTION_INFORMATION, *PWER_EXCEPTION_INFORMATION
req.redist: 
---

# WER_EXCEPTION_INFORMATION structure


## -description


Contains exception information for the <a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a> function.


## -struct-fields




### -field pExceptionPointers

A pointer to an <a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure.


### -field bClientPointers

A process (calling process) can provide error reporting functionality for another process (client process). If this member is <b>TRUE</b>, the exception pointer is located inside the  address space of the client process. If this member is <b>FALSE</b>, the exception pointer is located inside the address space of the calling process.


## -see-also




<a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a>
 

 

