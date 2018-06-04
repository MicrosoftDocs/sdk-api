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

# XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS structure


## -description


Defines stream buffer parameters that remain constant while an XAPO is locked. Used with the <a href="https://msdn.microsoft.com/e76c9fc5-15ed-497e-a7da-42b8e3642903">IXAPO::LockForProcess</a> method.


## -struct-fields




### -field pFormat

A WAVFORMATEX describing the format for the stream buffer.


### -field MaxFrameCount

Maximum number of frames in the stream buffer that <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> would ever be required to handle, irrespective of dynamic parameter settings.


## -remarks



The byte size of the respective stream buffer must be at least <i>MaxFrameCount</i> × (<i>pFormat</i>-&gt;nBlockAlign) bytes.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

