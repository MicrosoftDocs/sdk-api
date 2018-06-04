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

# IWMVideoMediaProps::SetQuality


## -description



The <b>SetQuality</b> method specifies the quality setting for the video stream.




## -parameters




### -param dwQuality [in]

<b>DWORD</b> specifying the quality setting, in the range from zero (maximum <a href="wmformat_glossary.htm">frame rate</a>) to 100 (maximum image quality).


## -returns



This method always returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/9edfe229-ffc5-4266-93af-1938bbd577c2">IWMVideoMediaProps::GetQuality</a>
 

 

