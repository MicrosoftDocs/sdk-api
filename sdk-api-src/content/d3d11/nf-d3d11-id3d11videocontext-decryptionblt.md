---
UID: NF:d3d11.ID3D11VideoContext.DecryptionBlt
title: ID3D11VideoContext::DecryptionBlt (d3d11.h)
description: Writes encrypted data to a protected surface. (ID3D11VideoContext.DecryptionBlt)
helpviewer_keywords: ["DecryptionBlt","DecryptionBlt method [Media Foundation]","DecryptionBlt method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","DecryptionBlt method","ID3D11VideoContext.DecryptionBlt","ID3D11VideoContext::DecryptionBlt","d3d11/ID3D11VideoContext::DecryptionBlt","mf.id3d11videocontext_decryptionblt"]
old-location: mf\id3d11videocontext_decryptionblt.htm
tech.root: mf
ms.assetid: E693D97A-E21F-4133-B56A-490F92CBD945
ms.date: 12/05/2018
ms.keywords: DecryptionBlt, DecryptionBlt method [Media Foundation], DecryptionBlt method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecryptionBlt method, ID3D11VideoContext.DecryptionBlt, ID3D11VideoContext::DecryptionBlt, d3d11/ID3D11VideoContext::DecryptionBlt, mf.id3d11videocontext_decryptionblt
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::DecryptionBlt
 - d3d11/ID3D11VideoContext::DecryptionBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.DecryptionBlt
---

# ID3D11VideoContext::DecryptionBlt


## -description

Writes encrypted data to a protected surface.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.

### -param pSrcSurface [in]

A pointer to the surface that contains the source data.

### -param pDstSurface [in]

A pointer to the protected surface where the encrypted data is written.

### -param pEncryptedBlockInfo [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_encrypted_block_info">D3D11_ENCRYPTED_BLOCK_INFO</a> structure, or <b>NULL</b>.

If the driver supports partially encrypted buffers,  <i>pEncryptedBlockInfo</i> indicates which portions of the buffer are encrypted.  If the entire surface is encrypted, set this parameter to <b>NULL</b>. 

To check whether the driver supports partially encrypted buffers, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_PARTIAL_DECRYPTION 
</b> capabilities flag. If the driver does not support partially encrypted buffers, set this parameter to <b>NULL</b>.

### -param ContentKeySize [in]

The size of the encrypted content key, in bytes.

### -param pContentKey [in]

A pointer to a buffer that contains a content encryption key, or <b>NULL</b>. To query whether the driver supports the use of content keys, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY</b> capabilities flag. 

If the driver supports content keys, use the content key to encrypt the surface. Encrypt the content key using the session key, and place the  resulting cipher text in <i>pContentKey</i>. If the driver does not support content keys, use the session key to encrypt the surface and set <i>pContentKey</i> to <b>NULL</b>.

### -param IVSize [in]

The size of the <i>pIV</i> buffer, in bytes.

### -param pIV [in]

A pointer to a buffer that contains the initialization vector (IV). 

For 128-bit AES-CTR encryption, <i>pIV</i> points to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_aes_ctr_iv">D3D11_AES_CTR_IV</a> structure. The caller allocates the structure and generates the IV. When you generate the first IV, initialize the structure to a random number. For each subsequent IV, simply increment the <b>IV</b> member of the structure, ensuring that the value always increases.  This procedure enables the driver to validate that the same IV is never used more than once with the same key pair.

For other encryption types, a different structure might be used, or the encryption might not use an IV.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Not all hardware or drivers support this functionality for all cryptographic types. This function can only be called when the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_content_protection_caps">D3D11_CONTENT_PROTECTION_CAPS_DECRYPTION_BLT</a>  cap is reported.

This method does not support writing to sub-rectangles of the surface.

If the hardware and driver support a content key:

<ul>
<li>The data is encrypted by the caller using the content key.</li>
<li>The content key is encrypted by the caller using the session key.</li>
<li>The encrypted content key is passed to the driver.</li>
</ul>
  Otherwise, the data is encrypted by the caller using the session key and NULL is passed as the content key.

If the driver and hardware support partially encrypted buffers, <i>pEncryptedBlockInfo</i> indicates which portions of the buffer are encrypted and which is not.  If the entire buffer is encrypted, <i>pEncryptedBlockinfo</i> should be <b>NULL</b>.

The <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_encrypted_block_info">D3D11_ENCRYPTED_BLOCK_INFO</a> allows the application to indicate which bytes in the buffer are encrypted.  This is specified in bytes, so the application must ensure that the encrypted blocks match the GPU’s crypto block alignment.

This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11 queries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
