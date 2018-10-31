---
UID: NS:d3d11_1.D3D11_VIDEO_DECODER_BUFFER_DESC1
title: D3D11_VIDEO_DECODER_BUFFER_DESC1
author: windows-sdk-content
description: Describes a compressed buffer for decoding.
old-location: mf\d3d11_video_decoder_buffer_desc1.htm
tech.root: medfound
ms.assetid: B35E4E27-6D69-49D4-908E-6EBF6DF5689A
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D3D11_VIDEO_DECODER_BUFFER_DESC1, D3D11_VIDEO_DECODER_BUFFER_DESC1 structure [Media Foundation], d3d11_1/D3D11_VIDEO_DECODER_BUFFER_DESC1, mf.d3d11_video_decoder_buffer_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_DECODER_BUFFER_DESC1
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_BUFFER_DESC1
req.redist: 
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

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dn894121(v=VS.85).aspx">D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK</a> structures, which indicates exactly which bytes in the decode buffer are encrypted and which are in the clear.  If the decode buffer does not contain encrypted data, set this member to NULL.

Values in the sub sample mapping blocks are relative to the start of the decode buffer.


### -field SubSampleMappingCount

The number of <a href="https://msdn.microsoft.com/en-us/library/Dn894121(v=VS.85).aspx">D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK</a> structures specified in the <i>pSubSampleMappingBlocks</i> parameter. If <i>pSubSampleMappingBlocks</i> is NULL, set this member to zero.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447680(v=VS.85).aspx">Direct3D 11 Video Structures</a>
 

 

