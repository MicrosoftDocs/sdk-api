---
UID: NF:d3d11_4.ID3D11VideoContext2.VideoProcessorSetStreamHDRMetaData
title: ID3D11VideoContext2::VideoProcessorSetStreamHDRMetaData
author: windows-sdk-content
description: Sets the HDR metadata associated with the video stream.
old-location: mf\id3d11videocontext2_videoprocessorsetstreamhdrmetadata.htm
tech.root: medfound
ms.assetid: C76CD8EF-3FBF-48B5-9633-BB65840BE34F
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: ID3D11VideoContext2 interface [Media Foundation],VideoProcessorSetStreamHDRMetaData method, ID3D11VideoContext2.VideoProcessorSetStreamHDRMetaData, ID3D11VideoContext2::VideoProcessorSetStreamHDRMetaData, VideoProcessorSetStreamHDRMetaData, VideoProcessorSetStreamHDRMetaData method [Media Foundation], VideoProcessorSetStreamHDRMetaData method [Media Foundation],ID3D11VideoContext2 interface, d3d11_4/ID3D11VideoContext2::VideoProcessorSetStreamHDRMetaData, mf.id3d11videocontext2_videoprocessorsetstreamhdrmetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoContext2.VideoProcessorSetStreamHDRMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext2::VideoProcessorSetStreamHDRMetaData


## -description


Sets the HDR metadata associated with the video stream.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Identifies the input stream.


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



When processing an HDR stream, the driver may use this information to tone map the video content to optimize it for the output display.




## -see-also




<a href="https://msdn.microsoft.com/E3FB5478-31CD-4AE3-BEA0-18823C4A4D3E">ID3D11VideoContext2</a>



<a href="mf.id3dvideocontext2">ID3DVideoContext2</a>
 

 

