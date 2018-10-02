---
UID: NS:d3d11.D3D11_ENCRYPTED_BLOCK_INFO
title: D3D11_ENCRYPTED_BLOCK_INFO
author: windows-sdk-content
description: Specifies which bytes in a video surface are encrypted.
old-location: mf\d3d11_encrypted_block_info.htm
tech.root: MedFound
ms.assetid: C52E2007-1E2B-4259-BE32-A96BB439F7C0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: D3D11_ENCRYPTED_BLOCK_INFO, D3D11_ENCRYPTED_BLOCK_INFO structure [Media Foundation], d3d11/D3D11_ENCRYPTED_BLOCK_INFO, mf.d3d11_encrypted_block_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_ENCRYPTED_BLOCK_INFO
product: Windows
targetos: Windows
req.typenames: D3D11_ENCRYPTED_BLOCK_INFO
req.redist: 
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




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/39010E57-FFF2-4793-B839-E336E8D2C1B2">ID3D11VideoContext::SubmitDecoderBuffers</a>
 

 

