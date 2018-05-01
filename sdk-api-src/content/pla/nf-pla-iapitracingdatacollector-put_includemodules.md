---
UID: NF:pla.IApiTracingDataCollector.put_IncludeModules
title: IApiTracingDataCollector::put_IncludeModules method
author: windows-driver-content
description: Retrieves or sets the list of modules to include in the trace.
old-location: pla\iapitracingdatacollector_includemodules.htm
old-project: PLA
ms.assetid: ec97533c-88a7-4360-bc2d-8e6465256032
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IApiTracingDataCollector, IApiTracingDataCollector interface [PLA], IncludeModules property, IApiTracingDataCollector.IncludeModules, IApiTracingDataCollector::get_IncludeModules, IApiTracingDataCollector::put_IncludeModules, IncludeModules property [PLA], IncludeModules property [PLA], IApiTracingDataCollector interface, base.iapitracingdatacollector_includemodules, pla.iapitracingdatacollector_includemodules, pla/IApiTracingDataCollector::IncludeModules, pla/IApiTracingDataCollector::get_IncludeModules, pla/IApiTracingDataCollector::put_IncludeModules, put_IncludeModules,IApiTracingDataCollector.put_IncludeModules
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IApiTracingDataCollector.IncludeModules
-	IApiTracingDataCollector.get_IncludeModules
-	IApiTracingDataCollector.put_IncludeModules
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IApiTracingDataCollector::put_IncludeModules method


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




<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>



<a href="https://msdn.microsoft.com/aa2239f0-b70e-491f-8a88-b41d429e8bb2">IApiTracingDataCollector::ExePath</a>
 

 

