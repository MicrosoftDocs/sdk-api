---
UID: NS:d3d11.D3D11_VIDEO_DECODER_EXTENSION
title: D3D11_VIDEO_DECODER_EXTENSION (d3d11.h)
author: windows-sdk-content
description: Contains driver-specific data for the ID3D11VideoContext::DecoderExtension method.
old-location: mf\d3d11_video_decoder_extension.htm
tech.root: medfound
ms.assetid: F82746A4-16AB-49B5-96C8-777675416467
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_VIDEO_DECODER_EXTENSION, D3D11_VIDEO_DECODER_EXTENSION structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_EXTENSION, mf.d3d11_video_decoder_extension
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_EXTENSION
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_EXTENSION
req.redist: 
---

# D3D11_VIDEO_DECODER_EXTENSION structure


## -description


Contains driver-specific data for the <a href="https://msdn.microsoft.com/B96FD793-C82A-4752-8F59-3CC9B86D1C2D">ID3D11VideoContext::DecoderExtension</a> method.


## -struct-fields




### -field Function

The function number. This number identifies the operation to perform. Currently no function numbers are defined.


### -field pPrivateInputData

A pointer to a buffer that contains input data for the driver.




### -field PrivateInputDataSize

The size of the <b>pPrivateInputData</b> buffer, in bytes.


### -field pPrivateOutputData

A pointer to a buffer that the driver can use to write output data.


### -field PrivateOutputDataSize

The size of the <b>pPrivateOutputData</b> buffer, in bytes.


### -field ResourceCount

The number of elements in the <b>ppResourceList</b> array. If <b>ppResourceList</b> is <b>NULL</b>, set <b>ResourceCount</b> to zero.


### -field ppResourceList

The address of an array of <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> pointers. Use this member to pass Direct3D resources to the driver.


## -remarks



The exact meaning of each structure member depends on the value of <b>Function</b>.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

