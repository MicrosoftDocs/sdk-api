---
UID: NF:amsi.AmsiUninitialize
title: AmsiUninitialize function
author: windows-sdk-content
description: Remove the instance of the AMSI API that was originally opened by AmsiInitialize.
old-location: amsi\amsiuninitialize.htm
tech.root: AMSI
ms.assetid: DAC1AAE6-3160-4A82-8E81-9CB245AFD653
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AmsiUninitialize, AmsiUninitialize function [Antimalware Scan Interface], amsi.amsiuninitialize, amsi/AmsiUninitialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
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
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AmsiUninitialize
: 
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
 

 

