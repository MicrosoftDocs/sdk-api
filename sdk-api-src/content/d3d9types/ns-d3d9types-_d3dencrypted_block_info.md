---
UID: NS:d3d9types._D3DENCRYPTED_BLOCK_INFO
title: "_D3DENCRYPTED_BLOCK_INFO"
author: windows-driver-content
description: Specifies which bytes are encrypted in a protected video surface.
old-location: mf\d3dencrypted_block_info.htm
old-project: medfound
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DENCRYPTED_BLOCK_INFO, D3DENCRYPTED_BLOCK_INFO structure [Media Foundation], _D3DENCRYPTED_BLOCK_INFO, d3d9types/D3DENCRYPTED_BLOCK_INFO, mf.d3dencrypted_block_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: D3d9.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DENCRYPTED_BLOCK_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DENCRYPTED_BLOCK_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DENCRYPTED_BLOCK_INFO structure


## -description


Specifies which bytes are encrypted in a protected video surface.


## -struct-fields




### -field NumEncryptedBytesAtBeginning

The number of bytes that are encrypted at the start of the buffer.


### -field NumBytesInSkipPattern

The number of bytes that are skipped after the first <b>NumEncryptedBytesAtBeginning</b> bytes, and then after each block of <b>NumBytesInEncryptPattern</b> bytes. Skipped bytes are not encrypted.


### -field NumBytesInEncryptPattern

The number of bytes that are encrypted after each block of skipped bytes.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>
 

 

