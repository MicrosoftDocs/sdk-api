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

# D3D11_VIDEO_DECODER_BUFFER_DESC1 structure


## -description


Describes a compressed buffer for decoding.


## -struct-fields




### -field BufferType

The type of buffer.


### -field DataOffset

The offset of the relevant data from the beginning of the buffer, in bytes. This value must be zero. 


### -field DataSize

Size of the relevant data.


### -field pIV

A pointer to a buffer that contains an initialization vector (IV) for encrypted data. If the decode buffer does not contain encrypted data, set this member to NULL.


### -field IVSize

The size of the buffer specified in the <i>pIV</i> parameter. If <i>pIV</i> is NULL, set this member to zero.


### -field pSubSampleMappingBlock

A pointer to an array of <a href="https://msdn.microsoft.com/82EC2598-60FB-4800-A001-0CCC2D0D529E">D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK</a> structures, which indicates exactly which bytes in the decode buffer are encrypted and which are in the clear.  If the decode buffer does not contain encrypted data, set this member to NULL.

Values in the sub sample mapping blocks are relative to the start of the decode buffer.


### -field SubSampleMappingCount

The number of <a href="https://msdn.microsoft.com/82EC2598-60FB-4800-A001-0CCC2D0D529E">D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK</a> structures specified in the <i>pSubSampleMappingBlocks</i> parameter. If <i>pSubSampleMappingBlocks</i> is NULL, set this member to zero.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

