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

# IVPConfig::SetScalingFactors


## -description



The <code>SetScalingFactors</code> method sets the factors by which the decoder should scale the video stream.




## -parameters




### -param pamvpSize [in]

Pointer to the new scaling size structure (<a href="https://msdn.microsoft.com/e36163bc-a7ea-421e-b876-2d459ecb11e8">AMVPSIZE</a>) to use to specify the width and height.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the decoder does not support the specified scaling factors, then it sets the values to the nearest factors it can support.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig Interface</a>
 

 

