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

# _DXVA2_AES_CTR_IV structure


## -description


Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.


## -struct-fields




### -field IV

The IV, in big-endian format.


### -field Count

The block count, in big-endian format.


## -remarks



For AES-CTR encyption, the <b>pvPVPState</b> member of the <a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a> structure points to a <b>DXVA2_AES_CTR_IV</b> structure.

The <a href="https://msdn.microsoft.com/2ee738c2-d56c-4a50-94b8-b7180918aa8c">D3DAES_CTR_IV</a> structure and the <b>DXVA2_AES_CTR_IV</b> structure are equivalent.

<h3><a id="Sequential_Counts"></a><a id="sequential_counts"></a><a id="SEQUENTIAL_COUNTS"></a>Sequential Counts</h3>
If the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> method returns the <b>D3DCPCAPS_SEQUENTIAL_CTR_IV</b> flag, the caller should keep <b>IV</b> unchanged when submitting multiple buffers for the same video frame, and <b>Count</b> should be in sequential order of the previous submission for the frame.

Example: Suppose the software decoder submits three buffers for a single frame, and that each buffer contains three 128-bit blocks.  For the first buffer, <b>IV</b> can be any value. For the next two buffers, the same value of <b>IV</b>  must be used. The value of  <b>Count</b> starts at 1. For the second buffer, <b>Count</b> equals 4 (1 + 3 blocks from the first submission). For the third buffer, <b>Count</b> equals 7 (4 + 3 blocks from the second submission).

When the <b>D3DCPCAPS_SEQUENTIAL_CTR_IV</b> capability is present, it is recommended to submit data in 128-bit blocks.




## -see-also




<a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

