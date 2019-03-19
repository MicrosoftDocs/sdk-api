---
UID: NS:amva._tag_AMVAEndFrameInfo
title: AMVAEndFrameInfo (amva.h)
author: windows-sdk-content
description: The AMVAEndFrameInfo structure contains information for the IAMVideoAccelerator::EndFrame method.
old-location: dshow\amvaendframeinfo.htm
tech.root: DirectShow
ms.assetid: 7f9308c1-0426-4c0f-97aa-4d946ac2403a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPAMVAEndFrameInfo, AMVAEndFrameInfo, AMVAEndFrameInfo structure [DirectShow], AMVAEndFrameInfoStructure, LPAMVAEndFrameInfo, LPAMVAEndFrameInfo structure pointer [DirectShow], amva/AMVAEndFrameInfo, amva/LPAMVAEndFrameInfo, dshow.amvaendframeinfo"
ms.topic: struct
req.header: amva.h
req.include-header: Videoacc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - amva.h
api_name:
 - AMVAEndFrameInfo
product: Windows
targetos: Windows
req.typenames: AMVAEndFrameInfo, *LPAMVAEndFrameInfo
req.redist: 
---

# AMVAEndFrameInfo structure


## -description


The <b>AMVAEndFrameInfo</b> structure contains information  for the <a href="https://msdn.microsoft.com/en-us/library/Dd376001(v=VS.85).aspx">IAMVideoAccelerator::EndFrame</a> method.


## -struct-fields




### -field dwSizeMiscData

Size, in bytes, of the buffer that <b>pMiscData</b> points to. The value must be 2.


### -field pMiscData

Pointer to a buffer that contains data for the video accelerator.

This buffer must contain a <b>WORD</b> value equal equal to the same surface index that passed to the corresponding <a href="https://msdn.microsoft.com/en-us/library/Dd375997(v=VS.85).aspx">IAMVideoAccelerator::BeginFrame</a> method.


## -remarks



The buffer pointed to by <b>pMiscData</b> cannot contain pointer values, because their addresses will not be valid in kernel mode, where frame processing occurs.
      




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376001(v=VS.85).aspx">IAMVideoAccelerator::EndFrame</a>
 

 

