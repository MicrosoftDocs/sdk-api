---
UID: NC:wincrypt.PFN_CMSG_EXPORT_MAIL_LIST
title: PFN_CMSG_EXPORT_MAIL_LIST (wincrypt.h)
description: Encrypts and exports the content encryption key for a mailing list recipient of an enveloped message.
helpviewer_keywords: ["PFN_CMSG_EXPORT_MAIL_LIST","PFN_CMSG_EXPORT_MAIL_LIST callback","PFN_CMSG_EXPORT_MAIL_LIST callback function [Security]","security.pfn_cmsg_export_mail_list","wincrypt/PFN_CMSG_EXPORT_MAIL_LIST"]
old-location: security\pfn_cmsg_export_mail_list.htm
tech.root: security
ms.assetid: 68a75714-cf47-40f9-95ab-e1ffc8936390
ms.date: 12/05/2018
ms.keywords: PFN_CMSG_EXPORT_MAIL_LIST, PFN_CMSG_EXPORT_MAIL_LIST callback, PFN_CMSG_EXPORT_MAIL_LIST callback function [Security], security.pfn_cmsg_export_mail_list, wincrypt/PFN_CMSG_EXPORT_MAIL_LIST
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
 - PFN_CMSG_EXPORT_MAIL_LIST
 - wincrypt/PFN_CMSG_EXPORT_MAIL_LIST
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
 - PFN_CMSG_EXPORT_MAIL_LIST
---

# PFN_CMSG_EXPORT_MAIL_LIST callback function


## -description

The <b>PFN_CMSG_EXPORT_MAIL_LIST</b> callback function encrypts and exports the content encryption key for a mailing list recipient of an enveloped message. <b>PFN_CMSG_EXPORT_MAIL_LIST</b> can be installed by using a <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a> <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This function is called by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> function when its <i>dwMsgType</i> parameter is set to <b>CMSG_ENVELOPED</b>.

## -parameters

### -param pContentEncryptInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure that contains the content encryption key.

### -param pMailListEncodeInfo [in]

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_mail_list_recipient_encode_info">CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</a> structure that specifies the key used to encrypt the content encryption key.

### -param pMailListEncryptInfo [in, out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_mail_list_encrypt_info">CMSG_MAIL_LIST_ENCRYPT_INFO</a> structure that contains the encrypted content encryption key.

### -param dwFlags [in]

This value is not used. Set it to zero.

### -param pvReserved

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>PFN_CMSG_EXPORT_MAIL_LIST</b> function must update the  <b>EncryptedKey</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_mail_list_encrypt_info">CMSG_MAIL_LIST_ENCRYPT_INFO</a> structure pointed to by the <i>pMailListEncryptInfo</i> parameter. This function must use the <b>pfnAlloc</b> and <b>pfnFree</b> members of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_content_encrypt_info">CMSG_CONTENT_ENCRYPT_INFO</a> structure pointed to by the <i>pContentEncryptInfo</i> parameter to manage memory for any values that it updates.

You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constants for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CMSG_OID_EXPORT_MAIL_LIST_FUNC or CMSG_OID_CAPI1_EXPORT_MAIL_LIST_FUNC</td>
<td>"CryptMsgDllExportMailList"</td>
</tr>
</table>
