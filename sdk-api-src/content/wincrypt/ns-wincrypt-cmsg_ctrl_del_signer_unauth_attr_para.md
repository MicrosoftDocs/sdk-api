---
UID: NS:wincrypt._CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
title: CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA (wincrypt.h)
description: Used to delete an unauthenticated attribute of a signer of a signed message.
helpviewer_keywords: ["*PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA","CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA","CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure [Security]","PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA","PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security]","_crypto2_cmsg_ctrl_del_signer_unauth_attr_para","security.cmsg_ctrl_del_signer_unauth_attr_para","wincrypt/CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA","wincrypt/PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA"]
old-location: security\cmsg_ctrl_del_signer_unauth_attr_para.htm
tech.root: security
ms.assetid: 729fbbe0-40c6-41e7-851f-6f93f47e8f4d
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure [Security], PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security], _crypto2_cmsg_ctrl_del_signer_unauth_attr_para, security.cmsg_ctrl_del_signer_unauth_attr_para, wincrypt/CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, wincrypt/PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA'
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
req.typenames: CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, *PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/_CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
 - PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
 - CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
 - wincrypt/CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
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
 - CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
---

# CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure


## -description

The <b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA</b> structure is used to delete an unauthenticated attribute of a signer of a signed message. This structure is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a> if the <i>dwCrlType</i> parameter is <b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR</b>.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwSignerIndex

Index of the signer in the <b>rgSigners</b> array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures in a signed message's <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure. The unauthenticated attribute for this signer is deleted.

### -field dwUnauthAttrIndex

Index of the element in the <b>rgUnauthAttr</b> array of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structure holding the unauthenticated attribute to be removed.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>