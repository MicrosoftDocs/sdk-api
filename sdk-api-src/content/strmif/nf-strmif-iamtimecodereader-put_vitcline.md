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

# IAMTimecodeReader::put_VITCLine


## -description



The <code>put_VITCLine</code> method specifies the vertical interval line that the timecode reader will use to read timecode.



This method is not implemented.


## -parameters




### -param Line [in]

Vertical line containing timecode information (valid lines are 11-20; 0 means autoselect).


## -returns



Returns E_NOTIMPL.




## -remarks



If VITC mode is specified in the <a href="https://msdn.microsoft.com/dd9f5310-b1c0-46ff-b038-d6a50ac400a2">IAMTimecodeReader::SetTCRMode</a> method, you must specify which line or lines will contain timecode information. To read VITC on specific multiple lines, the caller would make successive calls to <code>IAMTimecodeReader::put_VITCLine</code>, once for each line desired.

Set the high bit to add to the list of lines for readers that test across multiple lines.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>



<a href="https://msdn.microsoft.com/04eda79a-1301-4bc1-855e-1cb0c4451797">IAMTimecodeReader::get_VITCLine</a>
 

 

