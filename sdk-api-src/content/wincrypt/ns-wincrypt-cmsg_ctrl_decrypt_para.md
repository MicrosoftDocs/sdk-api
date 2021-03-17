---
UID: NS:wincrypt._CMSG_CTRL_DECRYPT_PARA
title: CMSG_CTRL_DECRYPT_PARA (wincrypt.h)
description: Contains information used to decrypt an enveloped message for a key transport recipient. This structure is passed to CryptMsgControl if the dwCtrlType parameter is CMSG_CTRL_DECRYPT.
helpviewer_keywords: ["*PCMSG_CTRL_DECRYPT_PARA","AT_KEYEXCHANGE","AT_SIGNATURE","CMSG_CTRL_DECRYPT_PARA","CMSG_CTRL_DECRYPT_PARA structure [Security]","PCMSG_CTRL_DECRYPT_PARA","PCMSG_CTRL_DECRYPT_PARA structure pointer [Security]","_crypto2_cmsg_ctrl_decrypt_para","security.cmsg_ctrl_decrypt_para","wincrypt/CMSG_CTRL_DECRYPT_PARA","wincrypt/PCMSG_CTRL_DECRYPT_PARA"]
old-location: security\cmsg_ctrl_decrypt_para.htm
tech.root: security
ms.assetid: eb9b1daa-b04f-419a-88e3-7c772f9e62eb
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CTRL_DECRYPT_PARA, AT_KEYEXCHANGE, AT_SIGNATURE, CMSG_CTRL_DECRYPT_PARA, CMSG_CTRL_DECRYPT_PARA structure [Security], PCMSG_CTRL_DECRYPT_PARA, PCMSG_CTRL_DECRYPT_PARA structure pointer [Security], _crypto2_cmsg_ctrl_decrypt_para, security.cmsg_ctrl_decrypt_para, wincrypt/CMSG_CTRL_DECRYPT_PARA, wincrypt/PCMSG_CTRL_DECRYPT_PARA'
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
req.typenames: CMSG_CTRL_DECRYPT_PARA, *PCMSG_CTRL_DECRYPT_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CTRL_DECRYPT_PARA
 - wincrypt/_CMSG_CTRL_DECRYPT_PARA
 - PCMSG_CTRL_DECRYPT_PARA
 - wincrypt/PCMSG_CTRL_DECRYPT_PARA
 - CMSG_CTRL_DECRYPT_PARA
 - wincrypt/CMSG_CTRL_DECRYPT_PARA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_CTRL_DECRYPT_PARA
---

# CMSG_CTRL_DECRYPT_PARA structure


## -description

The <b>CMSG_CTRL_DECRYPT_PARA</b> structure contains information used to decrypt an enveloped message for a key transport recipient. This structure is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> if the <i>dwCtrlType</i> parameter is CMSG_CTRL_DECRYPT.

For information about how CryptoAPI supports <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability, see the Remarks section of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hCryptProv

<a href="/windows/desktop/SecGloss/c-gly">Cryptographic service provider</a> (CSP) handle. The CNG function <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> is called to determine the union choice.

### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG <a href="/windows/desktop/SecGloss/c-gly">Cryptographic service provider</a> (CSP). The CNG function, <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a>, is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function, <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncrypttranslatehandle">NCryptTranslateHandle</a>, will be called to convert the CryptoAPI <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function.

### -field dwKeySpec

The private key to be used. This member is not used when the <i>hNCryptKey</i> member is used.  




The following <b>dwKeySpec</b> values are defined for the default provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to encrypt and decrypt session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.

</td>
</tr>
</table>
 

If <b>dwKeySpec</b> is zero, the default AT_KEYEXCHANGE is used.

### -field dwRecipientIndex

Index of the recipient in the message associated with the <b>hCryptProv</b> private key.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>