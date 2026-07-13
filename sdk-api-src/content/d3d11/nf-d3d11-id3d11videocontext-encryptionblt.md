---
UID: NF:d3d11.ID3D11VideoContext.EncryptionBlt
title: ID3D11VideoContext::EncryptionBlt (d3d11.h)
description: Reads encrypted data from a protected surface. (ID3D11VideoContext.EncryptionBlt)
helpviewer_keywords: ["EncryptionBlt","EncryptionBlt method [Media Foundation]","EncryptionBlt method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","EncryptionBlt method","ID3D11VideoContext.EncryptionBlt","ID3D11VideoContext::EncryptionBlt","d3d11/ID3D11VideoContext::EncryptionBlt","mf.id3d11videocontext_encryptionblt"]
old-location: mf\id3d11videocontext_encryptionblt.htm
tech.root: mf
ms.assetid: 2BBD0BC2-53D9-435E-835C-20A992118329
ms.date: 12/05/2018
ms.keywords: EncryptionBlt, EncryptionBlt method [Media Foundation], EncryptionBlt method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],EncryptionBlt method, ID3D11VideoContext.EncryptionBlt, ID3D11VideoContext::EncryptionBlt, d3d11/ID3D11VideoContext::EncryptionBlt, mf.id3d11videocontext_encryptionblt
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
 - ID3D11VideoContext::EncryptionBlt
 - d3d11/ID3D11VideoContext::EncryptionBlt
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
 - ID3D11VideoContext.EncryptionBlt
---

# ID3D11VideoContext::EncryptionBlt


## -description

Reads encrypted data from a protected surface.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface of the cryptographic session.

### -param pSrcSurface [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a> interface of the protected surface.

### -param pDstSurface [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a> interface of the surface that receives the encrypted data.

### -param IVSize [in]

The size of the <i>pIV</i> buffer, in bytes.

### -param pIV [in]

A pointer to a buffer that receives the initialization vector (IV). The caller allocates this buffer, but the driver generates the IV. 

For 128-bit AES-CTR encryption, <i>pIV</i> points to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_aes_ctr_iv">D3D11_AES_CTR_IV</a> structure. When the driver generates the first IV, it initializes the structure to a random number. For each subsequent IV, the driver simply increments the <b>IV</b> member of the structure, ensuring that the value always increases. The application can validate that the same IV is never used more than once with the same key pair.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Not all drivers support this method. To query the driver capabilities, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK</b> 
flag in the <b>Caps</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps">D3D11_VIDEO_CONTENT_PROTECTION_CAPS</a> structure.

Some drivers might require a separate key to decrypt the data that is read back. To check for this requirement, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK_KEY</b> 
flag. If this flag is present, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey">ID3D11VideoContext::GetEncryptionBltKey</a> to get the decryption key.

This method has the following limitations:

<ul>
<li>Reading back  sub-rectangles is not supported.</li>
<li>Reading back  partially encrypted surfaces is not supported.</li>
<li>The protected surface must be either an off-screen plain surface or a render target.</li>
<li>The destination surface must be a <a href="/windows/desktop/medfound/mf-sa-d3d11-usage">D3D11_USAGE_STAGING</a> resource.</li>
<li>The protected surface cannot be multisampled.</li>
<li>Stretching and colorspace conversion are not supported.</li>
</ul>

This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11 queries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
