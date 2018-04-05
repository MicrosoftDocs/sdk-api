---
UID: NF:pla.IApiTracingDataCollector.get_ExePath
title: IApiTracingDataCollector::get_ExePath method
author: windows-driver-content
description: Retrieves or sets the path to the executable file whose API calls you want to trace.
old-location: pla\iapitracingdatacollector_exepath.htm
old-project: PLA
ms.assetid: aa2239f0-b70e-491f-8a88-b41d429e8bb2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ExePath property [PLA], ExePath property [PLA], IApiTracingDataCollector interface, IApiTracingDataCollector, IApiTracingDataCollector interface [PLA], ExePath property, IApiTracingDataCollector.ExePath, IApiTracingDataCollector::get_ExePath, IApiTracingDataCollector::put_ExePath, base.iapitracingdatacollector_exepath, get_ExePath,IApiTracingDataCollector.get_ExePath, pla.iapitracingdatacollector_exepath, pla/IApiTracingDataCollector::ExePath, pla/IApiTracingDataCollector::get_ExePath, pla/IApiTracingDataCollector::put_ExePath
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
-	IApiTracingDataCollector.ExePath
-	IApiTracingDataCollector.get_ExePath
-	IApiTracingDataCollector.put_ExePath
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IApiTracingDataCollector::get_ExePath method


## -description


Retrieves or sets the path to the executable file whose API calls you want to trace.

This property is read/write.


## -parameters


## -remarks



If the executable file is currently running, the trace occurs the next time the executable file runs, not at this time.




## -see-also




<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>



<a href="https://msdn.microsoft.com/ec97533c-88a7-4360-bc2d-8e6465256032">IApiTracingDataCollector::IncludeModules</a>
 

 

