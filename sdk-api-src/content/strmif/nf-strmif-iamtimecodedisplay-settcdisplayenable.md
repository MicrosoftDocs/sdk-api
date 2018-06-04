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

# IAMTimecodeDisplay::SetTCDisplayEnable


## -description



The <code>SetTCDisplayEnable</code> method enables or disables an external device's timecode character output generator.




## -parameters




### -param State [in]

Value specifying whether to enable or disable the timecode character output generator. Specify OATRUE to enable or OAFALSE to disable.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method is not intended for rendering characters inside a filter graph, it is purely intended for hardware displays. Ensure that your external timecode reader or generator has display capability before trying to use this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2edfc260-5bb6-475d-b8af-252e7c7a8552">IAMTimecodeDisplay Interface</a>



<a href="https://msdn.microsoft.com/fe8bac4d-a271-47b3-9737-f115429b50aa">IAMTimecodeDisplay::GetTCDisplayEnable</a>
 

 

