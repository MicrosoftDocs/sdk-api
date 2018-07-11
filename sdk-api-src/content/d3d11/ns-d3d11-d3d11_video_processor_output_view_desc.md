---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
title: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
author: windows-sdk-content
description: Describes a video processor output view.
old-location: mf\d3d11_video_processor_output_view_desc.htm
old-project: medfound
ms.assetid: 8E0D44C1-220C-4E70-8A60-591AEBC16A2B
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC, D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC, mf.d3d11_video_processor_output_view_desc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure


## -description


Describes a video processor output view.


## -struct-fields




### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/EB334FA2-B174-45B2-8087-AAB72BB41795">D3D11_VPOV_DIMENSION</a> enumeration.


### -field Texture2D

A <a href="https://msdn.microsoft.com/DFABFB34-2622-4AB7-A87E-7E15F4D20E69">D3D11_TEX2D_VPOV</a> structure that identifies the texture resource for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2D</b>.


### -field Texture2DArray

A <a href="https://msdn.microsoft.com/DF059392-3E4B-45D2-A3CD-A0C61C8D628F">D3D11_TEX2D_ARRAY_VPOV</a> structure that identifies the texture array for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2DARRAY</b>.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/EC7AFE44-877C-4FB0-9E61-FCD504A334D3">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>
 

 

