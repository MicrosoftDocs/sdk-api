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
 

 

