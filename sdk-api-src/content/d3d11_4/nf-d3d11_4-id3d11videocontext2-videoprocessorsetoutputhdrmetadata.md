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

# ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData


## -description


Sets the HDR metadata describing the display on which the content will be presented.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param Type [in]

The type of HDR metadata supplied.


### -param Size [in]

The size of the HDR metadata supplied in <i>pHDRMetaData</i>.

For <b>DXGI_HDR_METADATA_TYPE_NONE</b>, the size should be 0.

For <b>DXGI_HDR_METADATA_TYPE_HDR10</b>, the size is <code>sizeof(DXGI_HDR_METADATA_HDR10)</code>.


### -param pHDRMetaData [in]

Pointer to the metadata information.

For <b>DXGI_HDR_METADATA_TYPE_NONE</b>, this should be NULL.

For <b>DXGI_HDR_METADATA_TYPE_HDR10</b>, this is a pointer to a <a href="https://msdn.microsoft.com/67A53A43-121F-4D83-AACC-D25D58123BE1">DXGI_HDR_METADATA_HDR10</a> structure.


## -returns



This function does not return a value.




## -remarks



When processing an HDR stream, the driver may use this metadata optimize the video for the output display.




## -see-also




<a href="https://msdn.microsoft.com/E3FB5478-31CD-4AE3-BEA0-18823C4A4D3E">ID3D11VideoContext2</a>



<a href="mf.id3dvideocontext2">ID3DVideoContext2</a>
 

 

