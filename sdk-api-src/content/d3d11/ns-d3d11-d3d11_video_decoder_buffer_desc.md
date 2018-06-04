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

# D3D11_VIDEO_DECODER_BUFFER_DESC structure


## -description


Describes a compressed buffer for decoding.


## -struct-fields




### -field BufferType

The type of buffer, specified as a member of the <a href="https://msdn.microsoft.com/328B833F-750A-4A88-9571-EAB0532064BD">D3D11_VIDEO_DECODER_BUFFER_TYPE</a> enumeration.


### -field BufferIndex

Reserved.


### -field DataOffset

The offset of the relevant data from the beginning of the buffer, in bytes. This value must be zero. 



### -field DataSize

 


### -field FirstMBaddress

The macroblock address of the first macroblock in the buffer. The macroblock address is given in raster scan order.



### -field NumMBsInBuffer

The number of macroblocks of data in the buffer. This count includes skipped macroblocks. 


### -field Width

Reserved. Set to zero.


### -field Height

Reserved. Set to zero.


### -field Stride

Reserved. Set to zero.


### -field ReservedBits

Reserved. Set to zero.


### -field pIV

A pointer to a buffer that contains an initialization vector (IV) for encrypted data. If the decode buffer does not contain encrypted data, set this member to <b>NULL</b>.


### -field IVSize

The size of the buffer specified in the <b>pIV</b> parameter. If <b>pIV</b> is <b>NULL</b>, set this member to zero.


### -field PartialEncryption

If <b>TRUE</b>, the video surfaces are partially encrypted.


### -field EncryptedBlockInfo

A <a href="https://msdn.microsoft.com/C52E2007-1E2B-4259-BE32-A96BB439F7C0">D3D11_ENCRYPTED_BLOCK_INFO</a> structure that specifies which bytes of the surface are encrypted.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/39010E57-FFF2-4793-B839-E336E8D2C1B2">ID3D11VideoContext::SubmitDecoderBuffers</a>
 

 

