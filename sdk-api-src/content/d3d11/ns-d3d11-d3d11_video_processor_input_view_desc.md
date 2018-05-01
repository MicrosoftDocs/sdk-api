---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC
title: D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC
author: windows-driver-content
description: Describes a video processor input view.
old-location: mf\d3d11_video_processor_input_view_desc.htm
old-project: medfound
ms.assetid: 69EDF918-355A-4277-9F7E-C08CF65E5418
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC, D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC, mf.d3d11_video_processor_input_view_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC structure


## -description


Describes a video processor input view.


## -struct-fields




### -field FourCC

The surface format. If zero, the driver uses the DXGI format that was used to create the resource. If you are using feature level 9, the value must be zero.


### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/65003974-F86E-4604-BA8D-262CA2674D53">D3D11_VPIV_DIMENSION</a> enumeration.


#### - Texture2D

A <a href="https://msdn.microsoft.com/F174DF16-6E2F-4AE1-80D9-7565F96DE03A">D3D11_TEX2D_VPIV</a> structure that identifies the texture resource.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/3245D2AF-74A1-4068-A0BC-577FD42B353E">ID3D11VideoDevice::CreateVideoProcessorInputView</a>
 

 

