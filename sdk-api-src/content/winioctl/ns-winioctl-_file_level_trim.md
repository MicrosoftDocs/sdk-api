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

# _FILE_LEVEL_TRIM structure


## -description


Used as input to the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a> control code.


## -struct-fields




### -field Key

Reserved. Set to zero (0).


### -field NumRanges

Number of <a href="https://msdn.microsoft.com/library/windows/hardware/hh406405">FILE_LEVEL_TRIM_RANGE</a> entries in 
      the <b>Ranges</b> member. On return should be compared with the 
      <b>NumRangesProcessed</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/hh406402">FILE_LEVEL_TRIM_OUTPUT</a> structure.


### -field Ranges

Array of ranges that describe the portions of the file that are to be trimmed.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh406402">FILE_LEVEL_TRIM_OUTPUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406405">FILE_LEVEL_TRIM_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a>
 

 

