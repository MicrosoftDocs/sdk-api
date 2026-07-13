---
UID: NF:d3d11_4.ID3D11VideoDevice2.NegotiateCryptoSessionKeyExchangeMT
title: ID3D11VideoDevice2::NegotiateCryptoSessionKeyExchangeMT
description: Verifies that ID3D11VideoContext::NegotiateCryptoSessionKeyExchange behaves as expected when called asynchronously.
ms.date: 06/12/2025
tech.root: direct3d11
helpviewer_keywords:
 - NegotiateCryptoSessionKeyExchangeMT
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d11_4.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D11VideoDevice2::NegotiateCryptoSessionKeyExchangeMT
 - d3d11_4/ID3D11VideoDevice2::NegotiateCryptoSessionKeyExchangeMT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoDevice2::NegotiateCryptoSessionKeyExchangeMT
---

## -description

Verifies that [ID3D11VideoContext::NegotiateCryptoSessionKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) behaves as expected when called asynchronously.

## -parameters

### -param pCryptoSession

Type: \_In\_ **[ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession)\***

A pointer to the **ID3D11CryptoSession** interface of the cryptographic session.

### -param flags

Type: \_In\_ **D3D11_CRYPTO_SESSION_KEY_EXCHANGE_FLAGS**

Flags.

### -param DataSize

Type: \_In\_ **[UINT](/windows/win32/winprog/windows-data-type)**

The size of the *pData* byte array, in bytes.

### -param pData

Type: \_Inout\_updates\_bytes\_\(DataSize\) **[void](/windows/win32/winprog/windows-data-types)\***

A pointer to a byte array that contains the encrypted session key.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also

* [ID3D11VideoDevice2](./nn-d3d11_4-id3d11videodevice2.md)
