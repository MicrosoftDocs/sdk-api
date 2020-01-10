---
UID: NC:roerrorapi.PINSPECT_MEMORY_CALLBACK
title: PINSPECT_MEMORY_CALLBACK
description: Provides a function pointer to the callback used by the RoInspectCapturedStackBackTrace function.
old-location: winrt\pinspect_memory_callback.htm
tech.root: WinRT
ms.assetid: A5BF207D-BB8D-47C1-8D32-0B6494809E2B
ms.date: 12/5/2018
ms.keywords: PINSPECT_MEMORY_CALLBACK, PINSPECT_MEMORY_CALLBACK callback, PINSPECT_MEMORY_CALLBACK callback function [Windows Runtime], roerrorapi/PINSPECT_MEMORY_CALLBACK, winrt.pinspect_memory_callback
f1_keywords:
- roerrorapi/PINSPECT_MEMORY_CALLBACK
dev_langs:
- c++
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
- UserDefined
api_location:
- roerrorapi.h
api_name:
- PINSPECT_MEMORY_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
---

# PINSPECT_MEMORY_CALLBACK callback function


## -description


Provides a function pointer to the callback used by the <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace">RoInspectCapturedStackBackTrace</a> function.


## -parameters




### -param *context [in]

Custom context data provided to the <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace">RoInspectCapturedStackBackTrace</a> function.


### -param readAddress [in]

The address to read data from.


### -param length [in]

The number of bytes to read, starting at <i>readAddress</i>. 


### -param *buffer [out]

The buffer that receives a copy of the bytes that are read.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace">RoInspectCapturedStackBackTrace</a>
 

 

