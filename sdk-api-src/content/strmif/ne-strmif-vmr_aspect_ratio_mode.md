---
UID: NE:strmif.VMR_ASPECT_RATIO_MODE
title: VMR_ASPECT_RATIO_MODE
author: windows-sdk-content
description: The VMR_ASPECT_RATIO_MODE enumeration type describes whether the Video Mixing Renderer Filter 7 preserves the aspect ratio of the source video.
old-location: dshow\vmr_aspect_ratio_mode.htm
tech.root: DirectShow
ms.assetid: dd1d1d99-008b-4234-a38a-314ba02bb116
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VMR_ARMODE_LETTER_BOX, VMR_ARMODE_NONE, VMR_ASPECT_RATIO_MODE, VMR_ASPECT_RATIO_MODE , VMR_ASPECT_RATIO_MODE enumeration [DirectShow], VMR_ASPECT_RATIO_MODEEnumeration, dshow.vmr_aspect_ratio_mode, strmif/VMR_ARMODE_LETTER_BOX, strmif/VMR_ARMODE_NONE, strmif/VMR_ASPECT_RATIO_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
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
 - strmif.h
api_name:
 - VMR_ASPECT_RATIO_MODE
product: Windows
targetos: Windows
req.typenames: VMR_ASPECT_RATIO_MODE
req.redist: 
---

# VMR_ASPECT_RATIO_MODE enumeration


## -description



The <b>VMR_ASPECT_RATIO_MODE</b> enumeration type describes whether the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> preserves the aspect ratio of the source video.




## -enum-fields




### -field VMR_ARMODE_NONE

Indicates that the VMR will not try to maintain the aspect ratio of the source video.
          


### -field VMR_ARMODE_LETTER_BOX

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/a341be9d-9801-4215-840d-7d581e9ec3cb">IVMRAspectRatioControl Interface</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>
 

 

