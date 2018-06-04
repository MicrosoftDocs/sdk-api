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

# IFsrmReport::get_LastGeneratedFileNamePrefix


## -description


Retrieves the report's generated file name for the last time the report was run. The string is used to make the report name unique.

This property is read-only.


## -parameters


## -remarks



The file names are generated to identify the collection of files that were generated for a report job the last time the report job ran.

To determine where the reports are stored, access the <a href="https://msdn.microsoft.com/b72ce871-41e0-4321-8c9c-0ae77a02c7ff">IFsrmReportJob::LastGeneratedInDirectory</a> property.




## -see-also




<a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a>
 

 

