---
UID: NS:dxva2api._DXVA2_AES_CTR_IV
title: DXVA2_AES_CTR_IV (dxva2api.h)
description: Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption. (DXVA2_AES_CTR_IV)
helpviewer_keywords: ["DXVA2_AES_CTR_IV","DXVA2_AES_CTR_IV structure [Media Foundation]","dxva2api/DXVA2_AES_CTR_IV","mf.dxva2_aes_ctr_iv"]
old-location: mf\dxva2_aes_ctr_iv.htm
tech.root: mf
ms.assetid: acde4bbb-2a14-4237-b426-a157a9781f40
ms.date: 12/05/2018
ms.keywords: DXVA2_AES_CTR_IV, DXVA2_AES_CTR_IV structure [Media Foundation], dxva2api/DXVA2_AES_CTR_IV, mf.dxva2_aes_ctr_iv
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXVA2_AES_CTR_IV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_AES_CTR_IV
 - dxva2api/_DXVA2_AES_CTR_IV
 - DXVA2_AES_CTR_IV
 - dxva2api/DXVA2_AES_CTR_IV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_AES_CTR_IV
---

# DXVA2_AES_CTR_IV structure


## -description

Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.

## -struct-fields

### -field IV

The IV, in big-endian format.

### -field Count

The block count, in big-endian format.

## -remarks

For AES-CTR encryption, the <b>pvPVPState</b> member of the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc">DXVA2_DecodeBufferDesc</a> structure points to a <b>DXVA2_AES_CTR_IV</b> structure.

The <a href="/windows/desktop/medfound/d3daes-ctr-iv">D3DAES_CTR_IV</a> structure and the <b>DXVA2_AES_CTR_IV</b> structure are equivalent.

<h3><a id="Sequential_Counts"></a><a id="sequential_counts"></a><a id="SEQUENTIAL_COUNTS"></a>Sequential Counts</h3>
If the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a> method returns the <b>D3DCPCAPS_SEQUENTIAL_CTR_IV</b> flag, the caller should keep <b>IV</b> unchanged when submitting multiple buffers for the same video frame, and <b>Count</b> should be in sequential order of the previous submission for the frame.

Example: Suppose the software decoder submits three buffers for a single frame, and that each buffer contains three 128-bit blocks.  For the first buffer, <b>IV</b> can be any value. For the next two buffers, the same value of <b>IV</b>  must be used. The value of  <b>Count</b> starts at 1. For the second buffer, <b>Count</b> equals 4 (1 + 3 blocks from the first submission). For the third buffer, <b>Count</b> equals 7 (4 + 3 blocks from the second submission).

When the <b>D3DCPCAPS_SEQUENTIAL_CTR_IV</b> capability is present, it is recommended to submit data in 128-bit blocks.

## -see-also

<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc">DXVA2_DecodeBufferDesc</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
