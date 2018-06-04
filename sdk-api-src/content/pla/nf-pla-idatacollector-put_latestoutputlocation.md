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

# IDataCollector::put_LatestOutputLocation


## -description


Retrieves or sets the fully decorated file name that PLA used the last time it created the file.

This property is read/write.


## -parameters


## -remarks



Typically, you do not set this property. When the data collector starts, PLA sets this property using the value from the <a href="https://msdn.microsoft.com/c5453d16-4aa4-4c25-bfc7-514693317473">IDataCollector::OutputLocation</a> property.

You can set this property to empty if the file has been deleted.

For trace data collectors only, you can set this property to the name of the file to use. If it is not set, PLA creates it as it would for any other data collector.




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>



<a href="https://msdn.microsoft.com/c5453d16-4aa4-4c25-bfc7-514693317473">IDataCollector::OutputLocation</a>
 

 

