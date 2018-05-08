---
UID: NS:wincrypt._CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
title: "_CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA"
author: windows-driver-content
description: Used to delete an unauthenticated attribute of a signer of a signed message.
old-location: security\cmsg_ctrl_del_signer_unauth_attr_para.htm
old-project: SecCrypto
ms.assetid: 729fbbe0-40c6-41e7-851f-6f93f47e8f4d
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure [Security], PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security], _CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, _crypto2_cmsg_ctrl_del_signer_unauth_attr_para, security.cmsg_ctrl_del_signer_unauth_attr_para, wincrypt/CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, wincrypt/PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA"
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
req.typenames: CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA, *PCMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA structure


## -description


The <b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR_PARA</b> structure is used to delete an unauthenticated attribute of a signer of a signed message. This structure is passed to 
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> if the <i>dwCrlType</i> parameter is <b>CMSG_CTRL_DEL_SIGNER_UNAUTH_ATTR</b>.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwSignerIndex

Index of the signer in the <b>rgSigners</b> array of pointers to <a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures in a signed message's <a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure. The unauthenticated attribute for this signer is deleted.


### -field dwUnauthAttrIndex

Index of the element in the <b>rgUnauthAttr</b> array of the <a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structure holding the unauthenticated attribute to be removed.


## -see-also




<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
 

 

