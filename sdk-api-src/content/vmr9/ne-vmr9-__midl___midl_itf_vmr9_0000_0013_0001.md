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

# __MIDL___MIDL_itf_vmr9_0000_0013_0001 enumeration


## -description



The <code>VMR9DeinterlacePrefs</code> enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 9 (VMR-9) uses if the method set by the application cannot be used.




## -enum-fields




### -field DeinterlacePref9_NextBest

Use the next best mode offered by the driver.


### -field DeinterlacePref9_BOB

Use the bob method.


### -field DeinterlacePref9_Weave

Use the weave method (that is, no deinterlacing).


### -field DeinterlacePref9_Mask

Bitwise OR of the previous flags. This value is used internally by the VMR, and is not a valid flag.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>
 

 

