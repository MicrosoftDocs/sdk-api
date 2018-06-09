---
UID: NS:wincrypt._CRYPT_SMART_CARD_ROOT_INFO
title: "_CRYPT_SMART_CARD_ROOT_INFO"
author: windows-sdk-content
description: Contains the smart card and session IDs associated with a certificate context.
old-location: security\crypt_smart_card_root_info.htm
old-project: SecCrypto
ms.assetid: 165a1a9e-e426-4823-8d1b-f13c338964c9
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCRYPT_SMART_CARD_ROOT_INFO, CRYPT_SMART_CARD_ROOT_INFO, CRYPT_SMART_CARD_ROOT_INFO structure [Security], PCRYPT_SMART_CARD_ROOT_INFO, PCRYPT_SMART_CARD_ROOT_INFO structure pointer [Security], _CRYPT_SMART_CARD_ROOT_INFO, security.crypt_smart_card_root_info, wincrypt/CRYPT_SMART_CARD_ROOT_INFO, wincrypt/PCRYPT_SMART_CARD_ROOT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CRYPT_SMART_CARD_ROOT_INFO, *PCRYPT_SMART_CARD_ROOT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_SMART_CARD_ROOT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_SMART_CARD_ROOT_INFO structure


## -description


The <b>CRYPT_SMART_CARD_ROOT_INFO</b> structure contains the smart card and session IDs associated with a certificate context. The certificate propagation service uses this structure to transfer smart card data between a smart card and a virtual root certificate store on a computer.


## -struct-fields




### -field rgbCardID

An array of bytes that specify the smart card IDs retrieved by using the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function with the <i>dwParam</i> parameter set to <b>PP_SMARTCARD_GUID</b>.


### -field luid

A <a href="https://msdn.microsoft.com/5b61bbdd-a00a-4985-8066-574f9bff0079">ROOT_INFO_LUID</a> structure that specifies a session authentication ID from an access token.


## -remarks



The <b>luid</b> member value comes from the <b>AuthenticationId</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556849">TOKEN_STATISTICS</a> structure retrieved by calling the <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function.

A certificate context can include an array of multiple <b>CRYPT_SMART_CARD_ROOT_INFO</b> structures, one for each <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>) that the certificate propagation service has added to a root certificate.



