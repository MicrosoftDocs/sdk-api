---
UID: NF:d3d11.ID3D11VideoContext.EncryptionBlt
title: ID3D11VideoContext::EncryptionBlt
author: windows-driver-content
description: Reads encrypted data from a protected surface.
old-location: mf\id3d11videocontext_encryptionblt.htm
old-project: medfound
ms.assetid: 2BBD0BC2-53D9-435E-835C-20A992118329
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: EncryptionBlt, EncryptionBlt method [Media Foundation], EncryptionBlt method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],EncryptionBlt method, ID3D11VideoContext.EncryptionBlt, ID3D11VideoContext::EncryptionBlt, d3d11/ID3D11VideoContext::EncryptionBlt, mf.id3d11videocontext_encryptionblt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoContext.EncryptionBlt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::EncryptionBlt


## -description


Reads encrypted data from a protected surface.




## -parameters




### -param pCryptoSession [in]

A pointer to the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface of the cryptographic session.


### -param pSrcSurface [in]

A pointer to the <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a> interface of the protected surface.


### -param pDstSurface [in]

A pointer to the <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a> interface of the surface that receives the encrypted data.



### -param IVSize [in]

The size of the <i>pIV</i> buffer, in bytes.


### -param pIV [in]

A pointer to a buffer that receives the initialization vector (IV). The caller allocates this buffer, but the driver generates the IV. 

For 128-bit AES-CTR encryption, <i>pIV</i> points to a <a href="https://msdn.microsoft.com/2D1B24CA-6386-4406-9195-40913744C9CF">D3D11_AES_CTR_IV</a> structure. When the driver generates the first IV, it initializes the structure to a random number. For each subsequent IV, the driver simply increments the <b>IV</b> member of the structure, ensuring that the value always increases. The application can validate that the same IV is never used more than once with the same key pair.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Not all drivers support this method. To query the driver capabilities, call <a href="https://msdn.microsoft.com/3BF2D2B9-6A12-4E71-9F52-829BABA32EF6">ID3D11VideoDevice::GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK</b> 
flag in the <b>Caps</b> member of the <a href="https://msdn.microsoft.com/15691779-DC30-4C0C-86D0-497F2BD60614">D3D11_VIDEO_CONTENT_PROTECTION_CAPS</a> structure.

Some drivers might require a separate key to decrypt the data that is read back. To check for this requirement, call <a href="https://msdn.microsoft.com/library/windows/hardware/hh451656">GetContentProtectionCaps</a> and check for the <b>D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK_KEY</b> 
flag. If this flag is present, call <a href="https://msdn.microsoft.com/B62BE7CB-75FA-45E9-9AB7-83738DFE3B19">ID3D11VideoContext::GetEncryptionBltKey</a> to get the decryption key.

This method has the following limitations:

<ul>
<li>Reading back  sub-rectangles is not supported.</li>
<li>Reading back  partially encrypted surfaces is not supported.</li>
<li>The protected surface must be either an off-screen plain surface or a render target.</li>
<li>The destination surface must be a <a href="https://msdn.microsoft.com/E9A415FA-74BF-4822-BB0E-D8AAA7D73664">D3D11_USAGE_STAGING</a> resource.</li>
<li>The protected surface cannot be multisampled.</li>
<li>Stretching and colorspace conversion are not supported.</li>
</ul>
	This function does not honor a D3D11 predicate that may have been set.

	If the application uses <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11 quries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

