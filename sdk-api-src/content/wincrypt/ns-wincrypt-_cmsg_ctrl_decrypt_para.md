---
UID: NS:wincrypt._CMSG_CTRL_DECRYPT_PARA
title: "_CMSG_CTRL_DECRYPT_PARA"
author: windows-driver-content
description: Contains information used to decrypt an enveloped message for a key transport recipient. This structure is passed to CryptMsgControl if the dwCtrlType parameter is CMSG_CTRL_DECRYPT.
old-location: security\cmsg_ctrl_decrypt_para.htm
old-project: SecCrypto
ms.assetid: eb9b1daa-b04f-419a-88e3-7c772f9e62eb
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PCMSG_CTRL_DECRYPT_PARA, AT_KEYEXCHANGE, AT_SIGNATURE, CMSG_CTRL_DECRYPT_PARA, CMSG_CTRL_DECRYPT_PARA structure [Security], PCMSG_CTRL_DECRYPT_PARA, PCMSG_CTRL_DECRYPT_PARA structure pointer [Security], _CMSG_CTRL_DECRYPT_PARA, _crypto2_cmsg_ctrl_decrypt_para, security.cmsg_ctrl_decrypt_para, wincrypt/CMSG_CTRL_DECRYPT_PARA, wincrypt/PCMSG_CTRL_DECRYPT_PARA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CMSG_CTRL_DECRYPT_PARA, *PCMSG_CTRL_DECRYPT_PARA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_CTRL_DECRYPT_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_CTRL_DECRYPT_PARA structure


## -description


The <b>CMSG_CTRL_DECRYPT_PARA</b> structure contains information used to decrypt an enveloped message for a key transport recipient. This structure is passed to 
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> if the <i>dwCtrlType</i> parameter is CMSG_CTRL_DECRYPT.

For information about how CryptoAPI supports <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability, see the Remarks section of 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hCryptProv

<a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Cryptographic service provider</a> (CSP) handle. The CNG function <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a> is called to determine the union choice. 


### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Cryptographic service provider</a> (CSP). The CNG function, <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a>, is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function, <a href="https://msdn.microsoft.com/0c339864-b598-430c-a597-09d3571fdbb2">NCryptTranslateHandle</a>, will be called to convert the CryptoAPI <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.


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




<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
 

 

