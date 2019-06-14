---
UID: NC:dxmini.PDX_BOBNEXTFIELD
title: PDX_BOBNEXTFIELD (dxmini.h)
author: windows-sdk-content
description: The DxBobNextField callback function bobs the next field of interleaved data.
old-location: display\dxbobnextfield.htm
tech.root: display
ms.assetid: 5daafc0c-2a6d-45e2-8403-d54cb383b3b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DxBobNextField, DxBobNextField callback function [Display Devices], PDX_BOBNEXTFIELD, PDX_BOBNEXTFIELD callback, VideoMiniPort_DxApiFunctions_d95db457-005d-4eee-a110-19159f64008b.xml, display.dxbobnextfield, dxmini/DxBobNextField
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
ms.custom: 19H1
---

# PDX_BOBNEXTFIELD callback function


## -description


The <i>DxBobNextField</i> callback function bobs the next field of interleaved data. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - BobNextFieldInfo

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-_ddbobnextfieldinfo">DDBOBNEXTFIELDINFO</a> structure that contains the bob information for the surface.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxBobNextField</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:


<a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_GENERIC</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_OUTOFCAPS</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">DXERR_UNSUPPORTED</a>





## -remarks



When data is interleaved, the driver's <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a> function is called every other frame. This is insufficient for bob because it must be notified after every V-sync. The driver's <i>DxBobNextField</i> function is called when a V-sync does not cause a flip. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-_ddbobnextfieldinfo">DDBOBNEXTFIELDINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a>
 

 

