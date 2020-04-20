---
UID: NF:pla.IApiTracingDataCollector.get_IncludeModules
title: IApiTracingDataCollector::get_IncludeModules (pla.h)
description: Retrieves or sets the list of modules to include in the trace.helpviewer_keywords: ["IApiTracingDataCollector interface [PLA]","IncludeModules property","IApiTracingDataCollector.IncludeModules","IApiTracingDataCollector.get_IncludeModules","IApiTracingDataCollector::IncludeModules","IApiTracingDataCollector::get_IncludeModules","IApiTracingDataCollector::put_IncludeModules","IncludeModules property [PLA]","IncludeModules property [PLA]","IApiTracingDataCollector interface","base.iapitracingdatacollector_includemodules","get_IncludeModules","pla.iapitracingdatacollector_includemodules","pla/IApiTracingDataCollector::IncludeModules","pla/IApiTracingDataCollector::get_IncludeModules","pla/IApiTracingDataCollector::put_IncludeModules"]
old-location: pla\iapitracingdatacollector_includemodules.htm
tech.root: PLA
ms.assetid: ec97533c-88a7-4360-bc2d-8e6465256032
ms.date: 12/05/2018
ms.keywords: IApiTracingDataCollector interface [PLA],IncludeModules property, IApiTracingDataCollector.IncludeModules, IApiTracingDataCollector.get_IncludeModules, IApiTracingDataCollector::IncludeModules, IApiTracingDataCollector::get_IncludeModules, IApiTracingDataCollector::put_IncludeModules, IncludeModules property [PLA], IncludeModules property [PLA],IApiTracingDataCollector interface, base.iapitracingdatacollector_includemodules, get_IncludeModules, pla.iapitracingdatacollector_includemodules, pla/IApiTracingDataCollector::IncludeModules, pla/IApiTracingDataCollector::get_IncludeModules, pla/IApiTracingDataCollector::put_IncludeModules
f1_keywords:
- pla/IApiTracingDataCollector.IncludeModules
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
- IApiTracingDataCollector.IncludeModules
- IApiTracingDataCollector.get_IncludeModules
- IApiTracingDataCollector.put_IncludeModules
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApiTracingDataCollector::get_IncludeModules


## -description


Retrieves or sets the list of modules to include in the trace.

This property is read/write.


## -parameters


## -remarks



If you do not set this property, the trace will  include the following modules:

<ul>
<li>Advapi32.dll</li>
<li>Gdi32.dll</li>
<li>Kernel32.dll</li>
<li>User32.dll</li>
</ul>
This property  limits the  trace to a subset of those DLLs. For example, you can use this property to limit the trace to only Kernel32.dll and Advapi32.dll.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-iapitracingdatacollector-get_exepath">IApiTracingDataCollector::ExePath</a>
 

 

