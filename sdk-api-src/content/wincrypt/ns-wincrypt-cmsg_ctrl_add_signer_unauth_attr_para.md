---
UID: NS:wincrypt._CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
title: CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA (wincrypt.h)
description: Used to add an unauthenticated attribute to a signer of a signed message.
helpviewer_keywords: ["*PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA","CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA","CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure [Security]","PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA","PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security]","_crypto2_cmsg_ctrl_add_signer_unauth_attr_para","security.cmsg_ctrl_add_signer_unauth_attr_para","wincrypt/CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA","wincrypt/PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA"]
old-location: security\cmsg_ctrl_add_signer_unauth_attr_para.htm
tech.root: security
ms.assetid: 5e347a50-942e-4278-a9ae-ad4c30c55c6b
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure [Security], PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security], _crypto2_cmsg_ctrl_add_signer_unauth_attr_para, security.cmsg_ctrl_add_signer_unauth_attr_para, wincrypt/CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, wincrypt/PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA'
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
req.typenames: CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, *PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/_CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
 - PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
 - CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
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
 - CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
---

# CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure


## -description

The <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</b> structure is used to add an unauthenticated attribute to a signer of a signed message. This structure is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> if the <i>dwCtrlType</i> parameter is set to <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR</b>.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwSignerIndex

Index of the signer in the <b>rgSigners</b> array of pointers of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures in a signed message's 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure. The unauthenticated attribute is to be added to this signer's information.

### -field blob

### -field BLOB

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the encoded unauthenticated attribute as its <b>pbData</b> member.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>