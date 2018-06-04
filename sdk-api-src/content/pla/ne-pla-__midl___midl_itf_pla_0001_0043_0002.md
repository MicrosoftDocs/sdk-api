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

# __MIDL___MIDL_itf_pla_0001_0043_0002 enumeration


## -description


Defines the format of the data in the log file.


## -enum-fields




### -field plaCommaSeparated

Comma-separated log file. The first line in the text file contains column headings followed by comma-separated data in the remaining lines of the log file. 


### -field plaTabSeparated

Tab-separated log file. The first line in the text file contains column headings followed by tab-separated data in the remaining lines of the log file. 


### -field plaSql

The log contains SQL records. 


### -field plaBinary

Binary log file. 


## -see-also




<a href="https://msdn.microsoft.com/3b980ea6-cb08-4e10-b4b3-40fd504d5e8f">IPerformanceCounterDataCollector::LogFileFormat</a>
 

 

