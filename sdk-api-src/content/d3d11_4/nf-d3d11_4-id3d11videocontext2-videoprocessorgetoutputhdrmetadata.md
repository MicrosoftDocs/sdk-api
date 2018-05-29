---
UID: NF:d3d11_4.ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData
title: ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData
author: windows-sdk-content
description: Gets the HDR metadata describing the display on which the content will be presented.
old-location: mf\id3d11videocontext2_videoprocessorgetoutputhdrmetadata.htm
old-project: medfound
ms.assetid: 5739668F-DCF8-448C-8690-E254315B92AF
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ID3D11VideoContext2 interface [Media Foundation],VideoProcessorGetOutputHDRMetaData method, ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData, ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData, VideoProcessorGetOutputHDRMetaData, VideoProcessorGetOutputHDRMetaData method [Media Foundation], VideoProcessorGetOutputHDRMetaData method [Media Foundation],ID3D11VideoContext2 interface, d3d11_4/ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData, mf.id3d11videocontext2_videoprocessorgetoutputhdrmetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_4.h
api_name:
-	ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData


## -description


Gets the HDR metadata describing the display on which the content will be presented. 


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param pType




### -param Size [in]

The size of the memory referenced by <i>pHDRMetaData</i>.

If <i>pHDRMetaData</i> is NULL, <i>Size</i> should be 0.


### -param pMetaData






#### - Type [out]

The type of HDR metadata supplied.


#### - pHDRMetaData [out]

Pointer to a buffer that receives the HDR metadata.

This parameter can be NULL.


## -returns



This function does not return a value.




## -remarks



This can be called multiple times, the first time to get the <i>Type</i> (in which case <i>Size</i> can be 0 and <i>pHDRMetaData</i> can be NULL) and then again to with non-NULL values to retrieve the actual metadata.




## -see-also




<a href="https://msdn.microsoft.com/E3FB5478-31CD-4AE3-BEA0-18823C4A4D3E">ID3D11VideoContext2</a>



<a href="mf.id3dvideocontext2">ID3DVideoContext2</a>
 

 

