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

# IVPBaseConfig::GetMaxPixelRate


## -description



The <code>GetMaxPixelRate</code> method retrieves the maximum pixel rate the device will output for a given width and height.




## -parameters




### -param pamvpSize [in, out]

Pointer to an <a href="https://msdn.microsoft.com/e36163bc-a7ea-421e-b876-2d459ecb11e8">AMVPSIZE</a> structure containing the desired width and height.


### -param pdwMaxPixelsPerSecond [out]

Pointer to a variable that receives the maximum pixel rate, in pixels per second.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method retrieves the maximum pixels per second expected for a given size. If the device does not support this size, then it returns the rate and the size that it supports.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

