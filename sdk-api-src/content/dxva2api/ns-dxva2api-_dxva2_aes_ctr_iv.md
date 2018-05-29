---
UID: NS:dxva2api._DXVA2_AES_CTR_IV
title: "_DXVA2_AES_CTR_IV"
author: windows-sdk-content
description: Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.
old-location: mf\dxva2_aes_ctr_iv.htm
old-project: medfound
ms.assetid: acde4bbb-2a14-4237-b426-a157a9781f40
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DXVA2_AES_CTR_IV, DXVA2_AES_CTR_IV structure [Media Foundation], _DXVA2_AES_CTR_IV, dxva2api/DXVA2_AES_CTR_IV, mf.dxva2_aes_ctr_iv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva2api.h
req.include-header: 
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
req.typenames: DXVA2_AES_CTR_IV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva2api.h
api_name:
-	DXVA2_AES_CTR_IV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

