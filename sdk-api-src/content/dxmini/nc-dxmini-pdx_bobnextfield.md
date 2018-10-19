---
UID: NC:dxmini.PDX_BOBNEXTFIELD
title: PDX_BOBNEXTFIELD
author: windows-sdk-content
description: The DxBobNextField callback function bobs the next field of interleaved data.
old-location: display\dxbobnextfield.htm
tech.root: display
ms.assetid: 5daafc0c-2a6d-45e2-8403-d54cb383b3b7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: DxBobNextField, DxBobNextField callback function [Display Devices], PDX_BOBNEXTFIELD, PDX_BOBNEXTFIELD callback, VideoMiniPort_DxApiFunctions_d95db457-005d-4eee-a110-19159f64008b.xml, display.dxbobnextfield, dxmini/DxBobNextField
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxBobNextField
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_BOBNEXTFIELD callback function


## -description


The <i>DxBobNextField</i> callback function bobs the next field of interleaved data. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - BobNextFieldInfo

Points to a <a href="https://msdn.microsoft.com/fad2bf3d-798c-47d9-bd82-b6fc0deff0aa">DDBOBNEXTFIELDINFO</a> structure that contains the bob information for the surface.


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




<a href="https://msdn.microsoft.com/fad2bf3d-798c-47d9-bd82-b6fc0deff0aa">DDBOBNEXTFIELDINFO</a>



<a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a>
 

 

