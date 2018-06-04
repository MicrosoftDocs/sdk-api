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

# IConfigInterleaving::get_Interleaving


## -description



The <b>get_Interleaving</b> method gets the audio preroll time and the frequency of interleaving for an AVI file.




## -parameters




### -param prtInterleave [out]


            Receives the approximate duration of each interleaved group of audio or video chunks.


### -param prtPreroll [out]


            
            Receives the amount of audio data, in 100-nanosecond units, that is written to the file before the first video frame.
          
          


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/4b1363c4-9cdd-4b28-a5ea-e5e554597be2">IConfigInterleaving::put_Interleaving</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>



<a href="https://msdn.microsoft.com/4b1363c4-9cdd-4b28-a5ea-e5e554597be2">IConfigInterleaving::put_Interleaving</a>
 

 

