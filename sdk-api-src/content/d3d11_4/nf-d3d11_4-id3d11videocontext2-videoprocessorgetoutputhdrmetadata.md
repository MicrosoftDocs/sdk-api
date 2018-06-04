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
 

 

