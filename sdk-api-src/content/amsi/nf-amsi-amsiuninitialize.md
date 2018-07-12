---
UID: NF:amsi.AmsiUninitialize
title: AmsiUninitialize function
author: windows-sdk-content
description: Remove the instance of the AMSI API that was originally opened by AmsiInitialize.
old-location: amsi\amsiuninitialize.htm
old-project: AMSI
ms.assetid: DAC1AAE6-3160-4A82-8E81-9CB245AFD653
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: AmsiUninitialize, AmsiUninitialize function [Antimalware Scan Interface], amsi.amsiuninitialize, amsi/AmsiUninitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiUninitialize
product: Windows
targetos: Windows
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
---

# AmsiUninitialize function


## -description


Remove the instance of the AMSI API that was originally opened by <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>
 

 

