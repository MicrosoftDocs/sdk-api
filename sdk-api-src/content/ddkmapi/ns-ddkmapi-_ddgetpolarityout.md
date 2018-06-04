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

# _DDGETPOLARITYOUT structure


## -description


The DDGETPOLARITYOUT structure contains the requested polarity information. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff550660">DD_DXAPI_GET_POLARITY</a> operations. A return code of DD_OK indicates success.


### -field bPolarity

Specifies whether the field is an even or odd field of an interlaced video signal. A value of <b>TRUE</b> indicates even, <b>FALSE</b> indicates odd. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550660">DD_DXAPI_GET_POLARITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

