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

# PDX_BOBNEXTFIELD callback function


## -description


The <i>DxBobNextField</i> callback function bobs the next field of interleaved data. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - BobNextFieldInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549209">DDBOBNEXTFIELDINFO</a> structure that contains the bob information for the surface.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxBobNextField</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:


<a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">DXERR_GENERIC</a>



<a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">DXERR_OUTOFCAPS</a>



<a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">DXERR_UNSUPPORTED</a>





## -remarks



When data is interleaved, the driver's <a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a> function is called every other frame. This is insufficient for bob because it must be notified after every V-sync. The driver's <i>DxBobNextField</i> function is called when a V-sync does not cause a flip. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549209">DDBOBNEXTFIELDINFO</a>



<a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a>
 

 

