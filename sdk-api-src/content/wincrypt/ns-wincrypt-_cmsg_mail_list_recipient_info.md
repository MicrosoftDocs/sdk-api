---
UID: NS:wincrypt._CMSG_MAIL_LIST_RECIPIENT_INFO
title: "_CMSG_MAIL_LIST_RECIPIENT_INFO"
author: windows-sdk-content
description: Contains information used for previously distributed symmetric key-encryption keys (KEK).
old-location: security\cmsg_mail_list_recipient_info.htm
old-project: SecCrypto
ms.assetid: e0946278-75e9-4990-af81-d9e61da9724b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCMSG_MAIL_LIST_RECIPIENT_INFO, CMSG_MAIL_LIST_RECIPIENT_INFO, CMSG_MAIL_LIST_RECIPIENT_INFO structure [Security], PCMSG_MAIL_LIST_RECIPIENT_INFO, PCMSG_MAIL_LIST_RECIPIENT_INFO structure pointer [Security], _CMSG_MAIL_LIST_RECIPIENT_INFO, _crypto2_cmsg_mail_list_recipient_info, security.cmsg_mail_list_recipient_info, wincrypt/CMSG_MAIL_LIST_RECIPIENT_INFO, wincrypt/PCMSG_MAIL_LIST_RECIPIENT_INFO"
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
tech.root: 
req.typenames: CMSG_MAIL_LIST_RECIPIENT_INFO, *PCMSG_MAIL_LIST_RECIPIENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_MAIL_LIST_RECIPIENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_MAIL_LIST_RECIPIENT_INFO structure


## -description


The <b>CMSG_MAIL_LIST_RECIPIENT_INFO</b> structure contains information used for previously distributed <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric</a> key-encryption keys (KEK).


## -struct-fields




### -field dwVersion

Indicates the version of the structure. This member is always four.


### -field KeyId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that identifies a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a>-encryption key previously distributed to the sender and one or more recipients.


### -field KeyEncryptionAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encrypted content encryption key.


### -field Date

Optional. When present, this member specifies a single key-encryption key from a previously distributed set.


### -field pOtherAttr

Optional pointer to a 
<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure containing additional information.

