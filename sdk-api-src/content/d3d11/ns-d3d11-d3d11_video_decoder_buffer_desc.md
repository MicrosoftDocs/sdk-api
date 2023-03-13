---
UID: NS:d3d11.D3D11_VIDEO_DECODER_BUFFER_DESC
title: D3D11_VIDEO_DECODER_BUFFER_DESC (d3d11.h)
description: Describes a compressed buffer for decoding. (D3D11_VIDEO_DECODER_BUFFER_DESC)
helpviewer_keywords: ["D3D11_VIDEO_DECODER_BUFFER_DESC","D3D11_VIDEO_DECODER_BUFFER_DESC structure [Media Foundation]","d3d11/D3D11_VIDEO_DECODER_BUFFER_DESC","mf.d3d11_video_decoder_buffer_desc"]
old-location: mf\d3d11_video_decoder_buffer_desc.htm
tech.root: mf
ms.assetid: B7F10FD2-79D1-483F-A95A-4CA7BAC7434F
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_BUFFER_DESC, D3D11_VIDEO_DECODER_BUFFER_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_BUFFER_DESC, mf.d3d11_video_decoder_buffer_desc
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_BUFFER_DESC
 - d3d11/D3D11_VIDEO_DECODER_BUFFER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_BUFFER_DESC
---

# D3D11_VIDEO_DECODER_BUFFER_DESC structure


## -description

Describes a compressed buffer for decoding.

## -struct-fields

### -field BufferType

The type of buffer, specified as a member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_decoder_buffer_type">D3D11_VIDEO_DECODER_BUFFER_TYPE</a> enumeration.

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

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_encrypted_block_info">D3D11_ENCRYPTED_BLOCK_INFO</a> structure that specifies which bytes of the surface are encrypted.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers">ID3D11VideoContext::SubmitDecoderBuffers</a>
