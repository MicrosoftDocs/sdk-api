---
UID: NF:pla.IApiTracingDataCollector.put_ExePath
title: IApiTracingDataCollector::put_ExePath (pla.h)
description: Retrieves or sets the path to the executable file whose API calls you want to trace.
old-location: pla\iapitracingdatacollector_exepath.htm
tech.root: PLA
ms.assetid: aa2239f0-b70e-491f-8a88-b41d429e8bb2
ms.date: 12/05/2018
ms.keywords: ExePath property [PLA], ExePath property [PLA],IApiTracingDataCollector interface, IApiTracingDataCollector interface [PLA],ExePath property, IApiTracingDataCollector.ExePath, IApiTracingDataCollector.put_ExePath, IApiTracingDataCollector::ExePath, IApiTracingDataCollector::get_ExePath, IApiTracingDataCollector::put_ExePath, base.iapitracingdatacollector_exepath, pla.iapitracingdatacollector_exepath, pla/IApiTracingDataCollector::ExePath, pla/IApiTracingDataCollector::get_ExePath, pla/IApiTracingDataCollector::put_ExePath, put_ExePath
ms.topic: method
f1_keywords:
- pla/IApiTracingDataCollector.ExePath
dev_langs:
- c++
req.header: pla.h
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
req.dll: Pla.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Pla.dll
api_name:
- IApiTracingDataCollector.ExePath
- IApiTracingDataCollector.get_ExePath
- IApiTracingDataCollector.put_ExePath
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApiTracingDataCollector::put_ExePath


## -description


Retrieves or sets the path to the executable file whose API calls you want to trace.

This property is read/write.


## -parameters


## -remarks



If the executable file is currently running, the trace occurs the next time the executable file runs, not at this time.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-iapitracingdatacollector-get_includemodules">IApiTracingDataCollector::IncludeModules</a>
 

 

