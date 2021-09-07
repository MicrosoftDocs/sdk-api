---
UID: NF:d3d9.IDirect3DCryptoSession9.GetEncryptionBltKey
title: IDirect3DCryptoSession9::GetEncryptionBltKey (d3d9.h)
description: Gets the cryptographic key used to decrypt the data returned by the IDirect3DCryptoSession9::EncryptionBlt method.
helpviewer_keywords: ["GetEncryptionBltKey","GetEncryptionBltKey method [Media Foundation]","GetEncryptionBltKey method [Media Foundation]","IDirect3DCryptoSession9 interface","IDirect3DCryptoSession9 interface [Media Foundation]","GetEncryptionBltKey method","IDirect3DCryptoSession9.GetEncryptionBltKey","IDirect3DCryptoSession9::GetEncryptionBltKey","d3d9/IDirect3DCryptoSession9::GetEncryptionBltKey","mf.idirect3dcryptosession9_getencryptionbltkey"]
old-location: mf\idirect3dcryptosession9_getencryptionbltkey.htm
tech.root: mf
ms.assetid: c06b42b7-dc8a-4004-b2c5-37accc76db40
ms.date: 12/05/2018
ms.keywords: GetEncryptionBltKey, GetEncryptionBltKey method [Media Foundation], GetEncryptionBltKey method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetEncryptionBltKey method, IDirect3DCryptoSession9.GetEncryptionBltKey, IDirect3DCryptoSession9::GetEncryptionBltKey, d3d9/IDirect3DCryptoSession9::GetEncryptionBltKey, mf.idirect3dcryptosession9_getencryptionbltkey
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
 - IDirect3DCryptoSession9::GetEncryptionBltKey
 - d3d9/IDirect3DCryptoSession9::GetEncryptionBltKey
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
 - IDirect3DCryptoSession9.GetEncryptionBltKey
---

# IDirect3DCryptoSession9::GetEncryptionBltKey


## -description

Gets the cryptographic key used to decrypt the data returned by the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-encryptionblt">IDirect3DCryptoSession9::EncryptionBlt</a> method.

## -parameters

### -param pReadbackKey

A pointer to a byte array that receives the key. The key is encrypted using the session key.

### -param KeySize

The size of the <i>pReadbackKey</i> array, in bytes. The size should match the size of the session key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method applies only when the driver requires a separate content key for the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-encryptionblt">EncryptionBlt</a> method. If the driver requires a content key, it sets the <b>D3DCPCAPS_ENCRYPTEDREADBACKKEY</b> flag in the capabilities structure returned by the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a> method. Otherwise, the driver uses the session key to encrypt the data.

Each time this method is called, the driver generates a new key.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>