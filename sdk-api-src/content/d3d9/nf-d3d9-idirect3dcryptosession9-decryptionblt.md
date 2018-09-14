---
UID: NF:d3d9.IDirect3DCryptoSession9.DecryptionBlt
title: IDirect3DCryptoSession9::DecryptionBlt
author: windows-sdk-content
description: Writes encrypted data to a protected surface.
old-location: mf\idirect3dcryptosession9_decryptionblt.htm
tech.root: medfound
ms.assetid: 03032a3f-e10f-4f40-837e-01b7b113b29e
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DecryptionBlt, DecryptionBlt method [Media Foundation], DecryptionBlt method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],DecryptionBlt method, IDirect3DCryptoSession9.DecryptionBlt, IDirect3DCryptoSession9::DecryptionBlt, d3d9/IDirect3DCryptoSession9::DecryptionBlt, mf.idirect3dcryptosession9_decryptionblt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.DecryptionBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DCryptoSession9::DecryptionBlt


## -description


Writes encrypted data to a protected surface.


## -parameters




### -param pSrcSurface

A pointer to the surface that contains the source data.


### -param pDstSurface

A pointer to the protected surface where the encrypted data is written.


### -param SrcSurfaceSize

The size of the surface memory that <i>pSrcSurface</i> points to, in bytes. The size must be aligned to the value of <b>BlockAlignmentSize</b> in the driver capabilities structure; see Remarks.


### -param pEncryptedBlockInfo

A pointer to a <a href="https://msdn.microsoft.com/076f4f00-e86b-47e2-80dd-4d7434200138">D3DENCRYPTED_BLOCK_INFO</a> structure, or <b>NULL</b>.

If the driver supports partially encrypted buffers,  <i>pEncryptedBlockInfo</i> indicates which portions of the buffer are encrypted.  If the entire surface is encrypted, set this parameter to <b>NULL</b>. 

To check whether the driver supports partially encrypted buffers, call <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> and check for the <b>D3DCPCAPS_PARTIALDECRYPTION</b> capabilities flag. If the driver does not support partially encrypted buffers, set this parameter to <b>NULL</b>.


### -param pContentKey

A pointer to a buffer that contains a content encryption key, or <b>NULL</b>. To query whether the driver supports the use of content keys, call <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> and check for the <b>D3DCPCAPS_CONTENTKEY</b> capabilities flag. 

If the driver supports content keys, use the content key to encrypt the surface. Encrypt the content key using the session key, and place the  resulting cipher text in <i>pContentKey</i>. If the driver does not support content keys, use the session key to encrypt the surface and set <i>pContentKey</i> to <b>NULL</b>.


### -param pIV

A pointer to a buffer that contains the initialization vector (IV). 

If the encryption type is <b>D3DCRYPTOTYPE_AES128_CTR</b>, the buffer is a <a href="https://msdn.microsoft.com/2ee738c2-d56c-4a50-94b8-b7180918aa8c">D3DAES_CTR_IV</a> structure. The caller allocates the structure and generates the IV. When you generate the first IV, initialize the structure to a random number. For each subsequent IV, simply increment the <b>IV</b> member of the structure, ensuring that the value always increases.  This procedure enables the driver to validate that the same IV is never used more than once with the same key pair.

For other encryption types, a different structure might be used, or the encryption might not use an IV.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Not all hardware or drivers support this functionality for all cryptographic types.

The source surface must be a system memory surface created with the proper alignment restrictions.  The buffer must be large enough to accommodate the pitch and height of the protected surface, plus padding to accommodate the starting alignment restrictions and block transfer size.

Specifically, you should allocate the source surface as follows:

<ol>
<li>Call <a href="https://msdn.microsoft.com/7f9f637e-a693-4fc5-9bf9-a6900aa2ed8c">IDirect3DCryptoSession9::GetSurfacePitch</a> to get the stride of the protected surface.</li>
<li>Call the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> method to get the value of the <b>BufferAlignmentStart</b>  and <b>BlockAlignmentSize</b>  members in the <a href="https://msdn.microsoft.com/73ef2e12-d376-4bc2-a940-d421acfdd43e">D3DCONTENTPROTECTIONCAPS</a>  structure. </li>
<li>Calculate the minimum size of the surface memory as <i>SysMemSize</i> = protected surface stride × protected surface height.</li>
<li>Add padding to accommodate the values of <b>BufferAlignmentStart</b>  and <b>BlockAlignmentSize</b>.</li>
<li>Allocate a buffer in system memory, with size equal to <i>SysMemSize</i> (including padding). </li>
<li>If the address of the system memory buffer is not aligned to the value of <b>BufferAlignmentStart</b>, calculate a memory-aligned pointer that is an offset from the start of the buffer.</li>
<li>Call <a href="https://msdn.microsoft.com/03fd24f4-9db2-4763-b7c7-85c6d05c3c77">IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx</a> to create the source surface. Pass the memory-aligned pointer as the shared-resource handle (<i>pSharedHandle</i>).</li>
</ol>
If you lock the surface, the stride reported in the <a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a> structure might not match the stride of the protected surface. When you interpret the data, however, always use the stride of the protected surface.

This method does not support writing to subrectangles of the surface.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 

