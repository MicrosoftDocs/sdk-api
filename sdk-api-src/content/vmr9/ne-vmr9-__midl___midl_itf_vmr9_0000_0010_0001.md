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

# __MIDL___MIDL_itf_vmr9_0000_0010_0001 enumeration


## -description



The <b>VMR9Mode</b> enumeration type specifies the rendering mode of the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer 9</a> (VMR-9) filter. 




## -enum-fields




### -field VMR9Mode_Windowed

Windowed mode.


### -field VMR9Mode_Windowless

Windowless mode.


### -field VMR9Mode_Renderless

Renderless mode.


### -field VMR9Mode_Mask

Bitwise <b>OR</b> of all above flags; not used by applications.


## -remarks



For a description of the various VMR-9 modes, see <a href="https://msdn.microsoft.com/98244af1-5934-4d1c-b9c3-7a414b065fe7">VMR Modes of Operation</a>.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/e39077ce-737f-4dd9-ab7d-4dc087828fdf">IVMRFilterConfig9::GetRenderingMode</a>



<a href="https://msdn.microsoft.com/d7a27d7c-5cd4-4a20-ba15-7056d502e3e3">IVMRFilterConfig9::SetRenderingMode</a>
 

 

