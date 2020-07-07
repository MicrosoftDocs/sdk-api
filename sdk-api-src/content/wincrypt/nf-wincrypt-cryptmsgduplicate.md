---
UID: NF:wincrypt.CryptMsgDuplicate
title: CryptMsgDuplicate function (wincrypt.h)
description: The CryptMsgDuplicate function duplicates a cryptographic message handle by incrementing its reference count.
helpviewer_keywords: ["CryptMsgDuplicate","CryptMsgDuplicate function [Security]","_crypto2_cryptmsgduplicate","security.cryptmsgduplicate","wincrypt/CryptMsgDuplicate"]
old-location: security\cryptmsgduplicate.htm
tech.root: SecCrypto
ms.assetid: 9b1142b9-0caa-4304-bfe6-1c27c6a7b782
ms.date: 12/05/2018
ms.keywords: CryptMsgDuplicate, CryptMsgDuplicate function [Security], _crypto2_cryptmsgduplicate, security.cryptmsgduplicate, wincrypt/CryptMsgDuplicate
f1_keywords:
- wincrypt/CryptMsgDuplicate
dev_langs:
- c++
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CryptMsgDuplicate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptMsgDuplicate function


## -description


The <b>CryptMsgDuplicate</b> function duplicates a cryptographic message handle by incrementing its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a>.


## -parameters




### -param hCryptMsg [in]

Handle of the cryptographic message to be duplicated. Duplication is done by incrementing the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a> of the message. A copy of the message is not made.


## -returns



The returned handle is the same as the handle input. A copy of the message is not created. When you have finished using the duplicated message handle, decrease the reference count by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function.




## -remarks



<b>CryptMsgDuplicate</b> is used to increase the reference count on an <b>HCRYPTMSG</b> handle so that multiple calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> are required to actually release the handle.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/example-c-program-encoding-and-decoding-a-hashed-message">Example C Program: Encoding and Decoding a Hashed Message</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>
 

 

