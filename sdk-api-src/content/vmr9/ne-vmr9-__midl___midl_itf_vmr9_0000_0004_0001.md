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

# __MIDL___MIDL_itf_vmr9_0000_0004_0001 enumeration


## -description



The <code>VMR9AspectRatioMode</code> enumeration type is used with the <a href="https://msdn.microsoft.com/c18ab567-5e0d-400a-8dc1-e9ad83650b7c">IVMRWindowlessControl9::GetAspectRatioMode</a> and <a href="https://msdn.microsoft.com/5ba46490-0a82-495f-8742-d7a8efa95332">IVMRWindowlessControl9::SetAspectRatioMode</a> methods to set and retrieve the aspect ratio mode (VMR-9 only).




## -enum-fields




### -field VMR9ARMode_None

Indicates that the VMR is not attempting to maintain the aspect ratio of the source video.


### -field VMR9ARMode_LetterBox

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

