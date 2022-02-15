---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Decrypt
title: IWMSecureChannel::WMSC_Decrypt (wmsecure.h)
description: The WMSC_Decrypt method decrypts data across DLL boundaries.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_Decrypt method","IWMSecureChannel.WMSC_Decrypt","IWMSecureChannel::WMSC_Decrypt","WMSC_Decrypt","WMSC_Decrypt method [windows Media Format]","WMSC_Decrypt method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_decrypt","wmsecure/IWMSecureChannel::WMSC_Decrypt"]
old-location: wmformat\iwmsecurechannel_wmsc_decrypt.htm
tech.root: wmformat
ms.assetid: c477c1f9-0264-4d3f-8670-f0c52df9e6a6
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Decrypt method, IWMSecureChannel.WMSC_Decrypt, IWMSecureChannel::WMSC_Decrypt, WMSC_Decrypt, WMSC_Decrypt method [windows Media Format], WMSC_Decrypt method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_decrypt, wmsecure/IWMSecureChannel::WMSC_Decrypt
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IWMSecureChannel::WMSC_Decrypt
 - wmsecure/IWMSecureChannel::WMSC_Decrypt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel.WMSC_Decrypt
---

# IWMSecureChannel::WMSC_Decrypt


## -description

<p class="CCE_Message">[<b>WMSC_Decrypt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_Decrypt</b> method decrypts data across DLL boundaries

## -parameters

### -param pbData [in]

### -param cbData [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/wmsecure/nf-wmsecure-iwmsecurechannel-wmsc_encrypt">Encrypt</a> holds a lock on the connection which is released by <b>Decrypt</b>, so threads should not block between calls to encrypt
     and decrypt.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>