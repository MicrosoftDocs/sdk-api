---
UID: NS:d3d11.D3D11_ENCRYPTED_BLOCK_INFO
title: D3D11_ENCRYPTED_BLOCK_INFO (d3d11.h)
description: Specifies which bytes in a video surface are encrypted.
helpviewer_keywords: ["D3D11_ENCRYPTED_BLOCK_INFO","D3D11_ENCRYPTED_BLOCK_INFO structure [Media Foundation]","d3d11/D3D11_ENCRYPTED_BLOCK_INFO","mf.d3d11_encrypted_block_info"]
old-location: mf\d3d11_encrypted_block_info.htm
tech.root: mf
ms.assetid: C52E2007-1E2B-4259-BE32-A96BB439F7C0
ms.date: 12/05/2018
ms.keywords: D3D11_ENCRYPTED_BLOCK_INFO, D3D11_ENCRYPTED_BLOCK_INFO structure [Media Foundation], d3d11/D3D11_ENCRYPTED_BLOCK_INFO, mf.d3d11_encrypted_block_info
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
req.typenames: D3D11_ENCRYPTED_BLOCK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_ENCRYPTED_BLOCK_INFO
 - d3d11/D3D11_ENCRYPTED_BLOCK_INFO
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
 - D3D11_ENCRYPTED_BLOCK_INFO
---

# D3D11_ENCRYPTED_BLOCK_INFO structure


## -description

Specifies which bytes in a video surface are encrypted.

## -struct-fields

### -field NumEncryptedBytesAtBeginning

The number of bytes that are encrypted at the start of the buffer.

### -field NumBytesInSkipPattern

The number of bytes that are skipped after the first <b>NumEncryptedBytesAtBeginning</b> bytes, and then after each block of <b>NumBytesInEncryptPattern</b> bytes. Skipped bytes are not encrypted.

### -field NumBytesInEncryptPattern

The number of bytes that are encrypted after each block of skipped bytes.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers">ID3D11VideoContext::SubmitDecoderBuffers</a>