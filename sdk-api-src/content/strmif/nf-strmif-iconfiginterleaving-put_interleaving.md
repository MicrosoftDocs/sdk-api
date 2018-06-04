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

# IConfigInterleaving::put_Interleaving


## -description



The <b>put_Interleaving</b> method sets the audio preroll time and the frequency of interleaving for an AVI file.




## -parameters




### -param prtInterleave [in]


            The approximate duration of each interleaved group of audio or video chunks, in 100-nanosecond units.
          The exact amount of interleaving is also affected by the interleave mode, which is specified by calling <a href="https://msdn.microsoft.com/62b06dc2-2e71-4a14-82e5-63e921a3c11f">IConfigInterleaving::put_Mode</a>.


### -param prtPreroll [in]


            The amount of audio data, in 100-nanosecond units, that is written to the file before the first video frame.
          


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks




        An audio preroll of 750 milliseconds is recommended when authoring a file for distribution.
      

If you do not call this method, the default value for <i>prtInterleave</i> is 1000 milliseconds. The smaller the number, the larger the resulting file.
      




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>



<a href="https://msdn.microsoft.com/659aa136-c7fd-4955-913b-26f7c05325a8">IConfigInterleaving::get_Interleaving</a>
 

 

