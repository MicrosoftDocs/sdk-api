---
UID: NF:d3d11_4.ID3D11VideoContext2.VideoProcessorGetStreamHDRMetaData
title: ID3D11VideoContext2::VideoProcessorGetStreamHDRMetaData
author: windows-sdk-content
description: Gets the HDR metadata associated with the video stream.
old-location: mf\id3d11videocontext2_videoprocessorgetstreamhdrmetadata.htm
tech.root: medfound
ms.assetid: 08464EB5-8E1F-4E4B-A545-A18C82A0C921
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11VideoContext2 interface [Media Foundation],VideoProcessorGetStreamHDRMetaData method, ID3D11VideoContext2.VideoProcessorGetStreamHDRMetaData, ID3D11VideoContext2::VideoProcessorGetStreamHDRMetaData, VideoProcessorGetStreamHDRMetaData, VideoProcessorGetStreamHDRMetaData method [Media Foundation], VideoProcessorGetStreamHDRMetaData method [Media Foundation],ID3D11VideoContext2 interface, d3d11_4/ID3D11VideoContext2::VideoProcessorGetStreamHDRMetaData, mf.id3d11videocontext2_videoprocessorgetstreamhdrmetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_4.h
req.include-header: 
req.target-type: Windows
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
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoContext2.VideoProcessorGetStreamHDRMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11_4.h
: 
- ID3D11VideoContext2.VideoProcessorGetStreamHDRMetaData
: 
---

# ID3D11VideoContext2::VideoProcessorGetStreamHDRMetaData


## -description


Gets the HDR metadata associated with the video stream.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Identifies the input stream.


### -param pType [out]

The type of the HDR metadata currently associated with the stream.


### -param Size [in]

The size of the memory referenced by <i>pHDRMetaData</i>.

If <i>pHDRMetaData</i> is NULL, <i>Size</i> should be 0.


### -param pMetaData [out]

Pointer to a buffer that receives the HDR metadata.

This parameter can be NULL.


## -returns



This function does not return a value.




## -remarks



This can be called multiple times, the first time to get the <i>Type</i> (in which case <i>Size</i> can be 0 and <i>pHDRMetaData</i> can be NULL) and then again to with non-NULL values to retrieve the actual metadata.




## -see-also




<a href="https://msdn.microsoft.com/E3FB5478-31CD-4AE3-BEA0-18823C4A4D3E">ID3D11VideoContext2</a>



<a href="mf.id3dvideocontext2">ID3DVideoContext2</a>
 

 

