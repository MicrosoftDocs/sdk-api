---
UID: NF:d3d11.ID3D11VideoContext.GetEncryptionBltKey
title: ID3D11VideoContext::GetEncryptionBltKey (d3d11.h)
description: Gets the cryptographic key to decrypt the data returned by the ID3D11VideoContext::EncryptionBlt method.
helpviewer_keywords: ["GetEncryptionBltKey","GetEncryptionBltKey method [Media Foundation]","GetEncryptionBltKey method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","GetEncryptionBltKey method","ID3D11VideoContext.GetEncryptionBltKey","ID3D11VideoContext::GetEncryptionBltKey","d3d11/ID3D11VideoContext::GetEncryptionBltKey","mf.id3d11videocontext_getencryptionbltkey"]
old-location: mf\id3d11videocontext_getencryptionbltkey.htm
tech.root: mf
ms.assetid: B62BE7CB-75FA-45E9-9AB7-83738DFE3B19
ms.date: 12/05/2018
ms.keywords: GetEncryptionBltKey, GetEncryptionBltKey method [Media Foundation], GetEncryptionBltKey method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],GetEncryptionBltKey method, ID3D11VideoContext.GetEncryptionBltKey, ID3D11VideoContext::GetEncryptionBltKey, d3d11/ID3D11VideoContext::GetEncryptionBltKey, mf.id3d11videocontext_getencryptionbltkey
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
 - ID3D11VideoContext::GetEncryptionBltKey
 - d3d11/ID3D11VideoContext::GetEncryptionBltKey
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
 - ID3D11VideoContext.GetEncryptionBltKey
---

# ID3D11VideoContext::GetEncryptionBltKey


## -description

Gets the cryptographic key to decrypt the data returned by the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt">ID3D11VideoContext::EncryptionBlt</a> method.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.

### -param KeySize [in]

The size of the <i>pReadbackKey</i> array, in bytes. The size should match the size of the session key.

### -param pReadbackKey [out]

A pointer to a byte array that receives the key. The key is encrypted using the session key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method applies only when the driver requires a separate content key for the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt">EncryptionBlt</a> method. For more information, see the Remarks for <b>EncryptionBlt</b>.

Each time this method is called, the driver generates a new key.

The <i>KeySize</i> should match the size of the session key.

The read back key is encrypted by the driver/hardware using the session key.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>