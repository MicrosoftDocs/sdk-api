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

# IWMPServices::GetStreamTime


## -description



The <b>IWMPServices::GetStreamTime</b> method retrieves a structure indicating the current stream time.




## -parameters




### -param prt [in]

Pointer to a <b>REFERENCE_TIME</b> structure.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



The current stream time is determined by Windows Media Player. This means that the value returned by this method do not necessarily represent the elapsed time relative to the beginning of the file. For instance, if the user moves the trackbar in the Player to seek the media to a new position, the value returned by this method returns the time elapsed since the media began playing from the new position. Changes in playback rate will also affect the value returned by this method.

The values provided in the <b>rtTimestamp</b> member of <b>IMediaObject::ProcessInput</b> and the <b>rtTimestamp</b> member of the <b>DMO_OUTPUT_DATA_BUFFER</b> structure supplied by <b>IMediaObject::ProcessOutput</b> contain values that indicate when the data provided in the buffer will be rendered relative to the current stream time. Therefore, these values also do not necessarily represent the elapsed time relative to the beginning of the file file or the presentation time specified in the file.




## -see-also




<a href="https://msdn.microsoft.com/26d68b4b-4eeb-42e2-a1d1-0d0e73725059">IWMPServices Interface</a>
 

 

