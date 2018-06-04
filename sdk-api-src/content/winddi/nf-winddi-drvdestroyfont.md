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

# DrvDestroyFont function


## -description


The <b>DrvDestroyFont</b> function notifies the driver that a font realization is no longer needed and that the driver can now free any associated data structures it has allocated.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure that identifies the font instance.


## -returns



None




## -remarks



The <b>DrvDestroyFont</b> function is called only in font drivers and kernel-mode printer drivers. 

If the DEVICE_FONTTYPE flag is set in the <b>flFontType</b> member of the FONTOBJ structure, the driver should release any resources or memory identified with both the <b>pvConsumer</b> and <b>pvProducer</b> members of FONTOBJ. Otherwise, it should release only memory and resources identified with <b>pvConsumer</b>.

The driver must reset the <b>pvConsumer</b> and <b>pvProducer</b> members to <b>NULL</b> if it uses them.

GDI calls <b>DrvDestroyFont</b> once for the font producer and once again for the font consumer.

GDI guarantees that <b>DrvDestroyFont</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> never overlap; consequently, the driver can rely on cached information while processing a <b>DrvTextOut</b> call.

This function must be implemented if the font driver or kernel-mode printer driver allocates resources when it realizes fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

