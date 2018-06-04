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

# IVPBaseConfig::InformVPInputFormats


## -description



The <code>InformVPInputFormats</code> method informs the device what video formats the video port supports.




## -parameters




### -param dwNumFormats [in]

Number of video formats contained in the <i>pDDPixelFormats</i> parameter.


### -param pDDPixelFormats [in]

Pointer to an array of pixel format structures (<b>DDPIXELFORMAT</b>) to send to the device.


## -returns



Returns S_FALSE if failure, or S_OK otherwise.




## -remarks



The supplied array of supported video port formats might determine what formats the device, in turn, proposes.

The <b>DDPIXELFORMAT</b> structure is documented in the Windows DDK.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

