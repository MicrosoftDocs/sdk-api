---
UID: NE:strmif.VMRMode
title: VMRMode
author: windows-driver-content
description: The VMRMode enumeration type is used in calls to the IVMRFilterConfig::GetRenderingMode and IVMRFilterConfig::SetRenderingMode methods to retrieve or specify the Video Mixing Renderer Filter 7 (VMR-7) rendering mode.
old-location: dshow\vmrmode.htm
old-project: DirectShow
ms.assetid: cc924b1a-561f-4d62-8cc8-03ba5e5e8d5b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: VMRMode, VMRMode enumeration [DirectShow], VMRModeEnumeration, VMRMode_Mask, VMRMode_Renderless, VMRMode_Windowed, VMRMode_Windowless, dshow.vmrmode, strmif/VMRMode, strmif/VMRMode_Mask, strmif/VMRMode_Renderless, strmif/VMRMode_Windowed, strmif/VMRMode_Windowless
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VMRMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	VMRMode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# VMRMode enumeration


## -description



The <b>VMRMode</b> enumeration type is used in calls to the <a href="https://msdn.microsoft.com/139b0326-2ab1-4fa4-91ae-9115b4368660">IVMRFilterConfig::GetRenderingMode</a> and <a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">IVMRFilterConfig::SetRenderingMode</a> methods to retrieve or specify the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) rendering mode.




## -enum-fields




### -field VMRMode_Windowed


            Windowed mode.
          


### -field VMRMode_Windowless

Windowless mode.
          


### -field VMRMode_Renderless

Renderless mode.
          


### -field VMRMode_Mask

Bitwise <b>OR</b> of all above flags; this is not a valid value to pass to <a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">SetRenderingMode</a>.


## -remarks



These modes are mutually exclusive. The <b>VMRMode_Renderless</b> flag means that the application is providing its own allocator-presenter, which is responsible for all drawing to the screen. The <b>VMRMode_Windowed</b> flag is the default mode of the VMR-7. See <a href="https://msdn.microsoft.com/98244af1-5934-4d1c-b9c3-7a414b065fe7">VMR Modes of Operation</a> for more information on the rendering modes.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

