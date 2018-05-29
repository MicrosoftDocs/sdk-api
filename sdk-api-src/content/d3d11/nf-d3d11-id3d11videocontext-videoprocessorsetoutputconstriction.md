---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputConstriction
title: ID3D11VideoContext::VideoProcessorSetOutputConstriction
author: windows-sdk-content
description: Sets the amount of downsampling to perform on the output.
old-location: mf\id3d11videocontext_videoprocessorsetoutputconstriction.htm
old-project: medfound
ms.assetid: EA61A4B8-0853-4F17-B634-70A896DCF5F7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputConstriction method, ID3D11VideoContext.VideoProcessorSetOutputConstriction, ID3D11VideoContext::VideoProcessorSetOutputConstriction, VideoProcessorSetOutputConstriction, VideoProcessorSetOutputConstriction method [Media Foundation], VideoProcessorSetOutputConstriction method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputConstriction, mf.id3d11videocontext_videoprocessorsetoutputconstriction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoContext.VideoProcessorSetOutputConstriction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorSetOutputConstriction


## -description


Sets the amount of downsampling to perform on the output.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param Enable

If <b>TRUE</b>, downsampling is enabled. Otherwise, downsampling is disabled and the <b>Size</b> member is ignored. 


### -param Size

The sampling size.


## -returns



This method does not return a value.




## -remarks



Downsampling is sometimes used to reduce the quality of premium content when other forms of content protection are not available. By default, downsampling is disabled.

If the <i>Enable</i> parameter is <b>TRUE</b>, the driver downsamples the composed image  to the specified size, and then scales it back to the size of the target rectangle.

The width and height of <i>Size</i> must be greater than zero. If the size is larger than the target rectangle, downsampling does not occur.

To use this feature, the driver must support downsampling, indicated by the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION</b> capability flag. To query for this capability, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

