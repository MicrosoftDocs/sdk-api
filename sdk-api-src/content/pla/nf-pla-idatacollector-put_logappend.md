---
UID: NF:pla.IDataCollector.put_LogAppend
title: IDataCollector::put_LogAppend
author: windows-sdk-content
description: Retrieves or sets a value that indicates if PLA should append the collected data to the current file.
old-location: pla\idatacollector_logappend.htm
tech.root: PLA
ms.assetid: c9843647-2c36-4d08-98d0-4df63b054993
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDataCollector interface [PLA],LogAppend property, IDataCollector.LogAppend, IDataCollector.put_LogAppend, IDataCollector::LogAppend, IDataCollector::get_LogAppend, IDataCollector::put_LogAppend, LogAppend property [PLA], LogAppend property [PLA],IDataCollector interface, base.idatacollector_logappend, pla.idatacollector_logappend, pla/IDataCollector::LogAppend, pla/IDataCollector::get_LogAppend, pla/IDataCollector::put_LogAppend, put_LogAppend
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
 - IDataCollector.LogAppend
 - IDataCollector.get_LogAppend
 - IDataCollector.put_LogAppend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- pla.h
: 
- IDataCollector.put_LogAppend
: 
---

# IDataCollector::put_LogAppend


## -description


Retrieves or sets a value that indicates if PLA should append the collected data to the current file.

This property is read/write.


## -parameters


## -remarks



A validation error occurs if this property conflicts with the <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a> or <a href="https://msdn.microsoft.com/17f40639-2e24-4a7e-b934-036d8595bdbf">IDataCollector::LogOverwrite</a> properties. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>



<a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">IDataCollector::LogCircular</a>



<a href="https://msdn.microsoft.com/17f40639-2e24-4a7e-b934-036d8595bdbf">IDataCollector::LogOverwrite</a>
 

 

