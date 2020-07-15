---
UID: NF:wincrypt.CryptMsgClose
title: CryptMsgClose function (wincrypt.h)
description: The CryptMsgClose function closes a cryptographic message handle. At each call to this function, the reference count on the message is reduced by one. When the reference count reaches zero, the message is fully released.
helpviewer_keywords: ["CryptMsgClose","CryptMsgClose function [Security]","_crypto2_cryptmsgclose","security.cryptmsgclose","wincrypt/CryptMsgClose"]
old-location: security\cryptmsgclose.htm
tech.root: SecCrypto
ms.assetid: 2478dd60-233a-4ef3-86e9-62d2a59ab28a
ms.date: 12/05/2018
ms.keywords: CryptMsgClose, CryptMsgClose function [Security], _crypto2_cryptmsgclose, security.cryptmsgclose, wincrypt/CryptMsgClose
f1_keywords:
- wincrypt/CryptMsgClose
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
- CryptMsgClose
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptMsgClose function


## -description


The <b>CryptMsgClose</b> function closes a cryptographic message handle. At each call to this function, the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a> on the message is reduced by one. When the reference count reaches zero, the message is fully released.


## -parameters




### -param hCryptMsg [in]

Handle of the cryptographic message to be closed.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>
 

 

