---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDataCollectorSet::get_SubdirectoryFormat


## -description


Retrieves or sets flags that describe how to decorate the subdirectory name.

This property is read/write.


## -parameters


## -remarks



PLA appends the decoration to the folder name. For example, if you specify <b>plaMonthDayHour</b>, PLA appends the current month, day, and hour values to the folder name. If the folder name is MyFile, the result could be MyFile110816.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a>



<a href="https://msdn.microsoft.com/83b7df10-8b00-4d64-bf71-2c68e037ab3f">IDataCollectorSet::SubdirectoryFormatPattern</a>
 

 

