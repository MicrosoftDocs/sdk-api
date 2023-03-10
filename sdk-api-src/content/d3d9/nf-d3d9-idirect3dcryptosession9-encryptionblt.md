---
UID: NF:d3d9.IDirect3DCryptoSession9.EncryptionBlt
title: IDirect3DCryptoSession9::EncryptionBlt (d3d9.h)
description: Reads encrypted data from a protected surface. (IDirect3DCryptoSession9.EncryptionBlt)
helpviewer_keywords: ["EncryptionBlt","EncryptionBlt method [Media Foundation]","EncryptionBlt method [Media Foundation]","IDirect3DCryptoSession9 interface","IDirect3DCryptoSession9 interface [Media Foundation]","EncryptionBlt method","IDirect3DCryptoSession9.EncryptionBlt","IDirect3DCryptoSession9::EncryptionBlt","d3d9/IDirect3DCryptoSession9::EncryptionBlt","mf.idirect3dcryptosession9_encryptionblt"]
old-location: mf\idirect3dcryptosession9_encryptionblt.htm
tech.root: mf
ms.assetid: 42aa21d3-7c38-4058-b766-454be8b1ae80
ms.date: 12/05/2018
ms.keywords: EncryptionBlt, EncryptionBlt method [Media Foundation], EncryptionBlt method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],EncryptionBlt method, IDirect3DCryptoSession9.EncryptionBlt, IDirect3DCryptoSession9::EncryptionBlt, d3d9/IDirect3DCryptoSession9::EncryptionBlt, mf.idirect3dcryptosession9_encryptionblt
req.header: d3d9.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DCryptoSession9::EncryptionBlt
 - d3d9/IDirect3DCryptoSession9::EncryptionBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.EncryptionBlt
---

# IDirect3DCryptoSession9::EncryptionBlt


## -description

Reads encrypted data from a protected surface.

## -parameters

### -param pSrcSurface

Pointer to the protected surface.

### -param pDstSurface

Pointer to a surface that receives the encrypted data.

### -param DstSurfaceSize

The size of the surface memory that <i>pDstSurface</i> points to, in bytes. The size must be aligned to the value of <b>BlockAlignmentSize</b> in the driver capabilities structure; see Remarks.

### -param pIV

Pointer to a buffer that receives the initialization vector (IV). The caller allocates this buffer, but the driver generates the IV.

If the encryption type is <b>D3DCRYPTOTYPE_AES128_CTR</b> (128-bit AES-CTR), <i>pIV</i> points to a <a href="/windows/desktop/medfound/d3daes-ctr-iv">D3DAES_CTR_IV</a> structure. When the driver generates the first IV, it initializes the structure to a random number. For each subsequent IV, the driver simply increments the <b>IV</b> member of the structure, ensuring that the value always increases. This procedure enables the application to validate that the same IV is never used more than once with the same key pair.

For other encryption types, a different structure might be used, or the encryption might not use an IV.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the driver supports this method, it sets the <b>D3DCPCAPS_ENCRYPTEDREADBACK</b> flag in the capabilities structure returned by the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a> method.

If the driver sets the <b>D3DCPCAPS_ENCRYPTEDREADBACKKEY</b> capabilities flag, it means the driver uses a separate key to encrypt the data. To get this key, call the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getencryptionbltkey">IDirect3DCryptoSession9::GetEncryptionBltKey</a> method. Otherwise, the driver uses the session key to encrypt the data.

Allocate the destination surface (<i>pDstSurface</i>) as follows:

<ol>
<li>Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getsurfacepitch">IDirect3DCryptoSession9::GetSurfacePitch</a> to get the stride of the protected surface.</li>
<li>Call the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">GetContentProtectionCaps</a> method to get the value of the <b>BufferAlignmentStart</b>  and <b>BlockAlignmentSize</b>  members in the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps">D3DCONTENTPROTECTIONCAPS</a>  structure. </li>
<li>Calculate the minimum size of the surface memory as <i>SysMemSize</i> = protected surface stride × protected surface height.</li>
<li>Add padding to accommodate the values of <b>BufferAlignmentStart</b>  and <b>BlockAlignmentSize</b>.</li>
<li>Allocate a buffer in system memory, with size equal to <i>SysMemSize</i> (including padding). </li>
<li>If the address of the system memory buffer is not aligned to the value of <b>BufferAlignmentStart</b>, calculate a memory-aligned pointer that is an offset from the start of the buffer.</li>
<li>Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex">IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx</a> to create the destination surface. Pass the memory-aligned pointer as the shared-resource handle (<i>pSharedHandle</i>).</li>
</ol>
This method has the following limitations:

<ul>
<li>The method cannot read back  subrectangles or partially encrypted surfaces.</li>
<li>The protected surface must be either an offscreen plain surface or a render target.</li>
<li>The destination surface must be a system-memory surface, created with the proper alignment, as described earlier.</li>
<li>The protected surface cannot be multisampled.</li>
<li>The method does not support stretching or colorspace conversion.</li>
</ul>
If you lock the destination surface, the stride reported in the <a href="/windows/desktop/direct3d9/d3dlocked-rect">D3DLOCKED_RECT</a> structure might not match the stride of the protected surface. When you interpret the data, however, always use the stride of the protected surface.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
