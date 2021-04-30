---
UID: NC:wincrypt.PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
title: PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY (wincrypt.h)
description: Generates the symmetric key used to encrypt content for an enveloped message.
helpviewer_keywords: ["PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY","PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback","PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback function [Security]","security.pfn_cmsg_gen_content_encrypt_key","wincrypt/PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY"]
old-location: security\pfn_cmsg_gen_content_encrypt_key.htm
tech.root: security
ms.assetid: f06d0efb-44e1-40ed-9480-35dbdfce934c
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY, PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback, PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback function [Security], security.pfn_cmsg_gen_content_encrypt_key, wincrypt/PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
 - wincrypt/PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY
---

# PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY callback function


## -description

The <b>PFN_CMSG_GEN_CONTENT_ENCRYPT_KEY</b> callback function generates the symmetric key used to encrypt content for an enveloped message. This function is called by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function when it initializes the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure.

## -parameters

### -param pContentEncryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the key.

### -param dwFlags [in]

This value is not used. Set it to zero.

### -param pvReserved

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

You must define different callback functions for CAPI1 keys and Cryptography API: Next Generation (CNG) keys. Both functions have the same signature but use different <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs). Which function is called depends on the value of the  <b>fCNG</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the  <i>pContentEncryptInfo</i> parameter. The following table shows the relationship between the callback function and the value of the <b>fCNG</b> member.

<table>
<tr>
<th>fCNG value</th>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>CMSG_OID_GEN_CONTENT_ENCRYPT_KEY_FUNC or CMSG_OID_CAPI1_GEN_CONTENT_ENCRYPT_KEY_FUNC </td>
<td>"CryptMsgDllGenContentEncryptKey"</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>CMSG_OID_CNG_GEN_CONTENT_ENCRYPT_KEY_FUNC</td>
<td>"CryptMsgDllCNGGenContentEncryptKey"</td>
</tr>
</table>
