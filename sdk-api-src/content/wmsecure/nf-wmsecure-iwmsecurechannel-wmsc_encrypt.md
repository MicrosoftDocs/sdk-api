---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Encrypt
title: IWMSecureChannel::WMSC_Encrypt (wmsecure.h)
description: The WMSC_Encrypt method encrypts data across DLL boundaries.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_Encrypt method","IWMSecureChannel.WMSC_Encrypt","IWMSecureChannel::WMSC_Encrypt","WMSC_Encrypt","WMSC_Encrypt method [windows Media Format]","WMSC_Encrypt method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_encrypt","wmsecure/IWMSecureChannel::WMSC_Encrypt"]
old-location: wmformat\iwmsecurechannel_wmsc_encrypt.htm
tech.root: wmformat
ms.assetid: fdb90fbc-9504-4b72-83ab-b410c3bd2e1e
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Encrypt method, IWMSecureChannel.WMSC_Encrypt, IWMSecureChannel::WMSC_Encrypt, WMSC_Encrypt, WMSC_Encrypt method [windows Media Format], WMSC_Encrypt method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_encrypt, wmsecure/IWMSecureChannel::WMSC_Encrypt
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
 - IWMSecureChannel::WMSC_Encrypt
 - wmsecure/IWMSecureChannel::WMSC_Encrypt
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
 - IWMSecureChannel.WMSC_Encrypt
---

# IWMSecureChannel::WMSC_Encrypt


## -description

<p class="CCE_Message">[<b>WMSC_Encrypt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_Encrypt</b> method encrypts data across DLL boundaries.

## -parameters

### -param pbData [in]

### -param cbData [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Encrypt</b> holds a lock on the connection which is released by <a href="/windows/desktop/api/wmsecure/nf-wmsecure-iwmsecurechannel-wmsc_decrypt">Decrypt</a>, so threads should not block between calls to encrypt
     and decrypt.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>