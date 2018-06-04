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

# IIPDVDec::put_IPDisplay


## -description



The <code>put_IPDisplay</code> method sets the decoding resolution.




## -parameters




### -param displayPix [in]

Member of the <a href="https://msdn.microsoft.com/8ae9b402-e7cc-4e11-b956-974b53fd8934">DVDECODERRESOLUTION</a> enumerated type, specifying the decoding resolution. The meaning of this value depends on whether the current format is NTSC or PAL. The filter determines at run time which format applies, based on the media type.


## -returns



Returns S_OK if successful; otherwise, returns E_FAIL or another error code.




## -remarks



This method will fail if the filter is already streaming media data.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0e40841a-e297-4c05-aefa-7131de9c6a97">IIPDVDec Interface</a>
 

 

