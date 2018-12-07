---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0010_0001
title: "__MIDL___MIDL_itf_vmr9_0000_0010_0001"
author: windows-sdk-content
description: The VMR9Mode enumeration type specifies the rendering mode of the Video Mixing Renderer 9 (VMR-9) filter.
old-location: dshow\vmr9mode.htm
tech.root: DirectShow
ms.assetid: 708c45e4-e92b-4fe5-900f-7cd806011f5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VMR9Mode, VMR9Mode , VMR9Mode enumeration [DirectShow], VMR9ModeEnumeration, VMR9Mode_Mask, VMR9Mode_Renderless, VMR9Mode_Windowed, VMR9Mode_Windowless, __MIDL___MIDL_itf_vmr9_0000_0010_0001, dshow.vmr9mode, enumeration [DirectShow], vmr9/VMR9Mode, vmr9/VMR9Mode_Mask, vmr9/VMR9Mode_Renderless, vmr9/VMR9Mode_Windowed, vmr9/VMR9Mode_Windowless
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9Mode
product: Windows
targetos: Windows
req.typenames: VMR9Mode
req.redist: 
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
 

 

