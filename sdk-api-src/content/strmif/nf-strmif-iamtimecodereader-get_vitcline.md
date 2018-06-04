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

# IAMTimecodeReader::get_VITCLine


## -description



The <code>get_VITCLine</code> method retrieves the vertical interval line that the timecode reader is using to read timecode.



This method is not implemented.


## -parameters




### -param pLine [out]

Pointer to the vertical line containing timecode information (valid lines are from 11 through 20).


## -returns



Returns E_NOTIMPL.




## -remarks



The high bit indicates that multiple lines are used and successive calls will cycle through the line numbers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>



<a href="https://msdn.microsoft.com/171b0fd2-1498-41ae-9803-99b9128ee305">IAMTimecodeReader::put_VITCLine</a>
 

 

