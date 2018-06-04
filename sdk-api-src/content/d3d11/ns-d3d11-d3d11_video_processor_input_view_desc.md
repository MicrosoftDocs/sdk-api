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

# D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC structure


## -description


Describes a video processor input view.


## -struct-fields




### -field FourCC

The surface format. If zero, the driver uses the DXGI format that was used to create the resource. If you are using feature level 9, the value must be zero.


### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/65003974-F86E-4604-BA8D-262CA2674D53">D3D11_VPIV_DIMENSION</a> enumeration.


### -field Texture2D

A <a href="https://msdn.microsoft.com/F174DF16-6E2F-4AE1-80D9-7565F96DE03A">D3D11_TEX2D_VPIV</a> structure that identifies the texture resource.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/3245D2AF-74A1-4068-A0BC-577FD42B353E">ID3D11VideoDevice::CreateVideoProcessorInputView</a>
 

 

