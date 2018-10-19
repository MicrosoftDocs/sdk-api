---
UID: NS:wincrypt._CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
title: "_CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA"
author: windows-sdk-content
description: Used to add an unauthenticated attribute to a signer of a signed message.
old-location: security\cmsg_ctrl_add_signer_unauth_attr_para.htm
tech.root: seccrypto
ms.assetid: 5e347a50-942e-4278-a9ae-ad4c30c55c6b
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure [Security], PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure pointer [Security], _CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, _crypto2_cmsg_ctrl_add_signer_unauth_attr_para, security.cmsg_ctrl_add_signer_unauth_attr_para, wincrypt/CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, wincrypt/PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
product: Windows
targetos: Windows
req.typenames: CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA, *PCMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA
req.redist: 
---

# _CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA structure


## -description


The <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</b> structure is used to add an unauthenticated attribute to a signer of a signed message. This structure is passed to 
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> if the <i>dwCtrlType</i> parameter is set to <b>CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR</b>.
			


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwSignerIndex

Index of the signer in the <b>rgSigners</b> array of pointers of 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures in a signed message's 
<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure. The unauthenticated attribute is to be added to this signer's information.


### -field blob

 




#### - BLOB

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encoded unauthenticated attribute as its <b>pbData</b> member.


## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
 

 

