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

# _MFVideoDSPMode enumeration


## -description


Specifies the processing mode of the <a href="https://msdn.microsoft.com/BBC42190-08E4-4C3B-972A-FD30621A6CC1">Video Stabilization MFT</a>.


## -enum-fields




### -field MFVideoDSPMode_Passthrough

Pass-through mode. Video stabilization is not applied.


### -field MFVideoDSPMode_Stabilization

Video stabilization is applied.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/0D49892A-8628-4F2B-B41B-51160A19DC9B">MF_VIDEODSP_MODE</a> attribute.

In pass-through mode, the MFT does not apply any processing to the video.




## -see-also




<a href="https://msdn.microsoft.com/0D49892A-8628-4F2B-B41B-51160A19DC9B">MF_VIDEODSP_MODE</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/BBC42190-08E4-4C3B-972A-FD30621A6CC1">Video Stabilization MFT</a>
 

 

