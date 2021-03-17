---
UID: NS:wincrypt._CRYPT_SMART_CARD_ROOT_INFO
title: CRYPT_SMART_CARD_ROOT_INFO (wincrypt.h)
description: Contains the smart card and session IDs associated with a certificate context.
helpviewer_keywords: ["*PCRYPT_SMART_CARD_ROOT_INFO","CRYPT_SMART_CARD_ROOT_INFO","CRYPT_SMART_CARD_ROOT_INFO structure [Security]","PCRYPT_SMART_CARD_ROOT_INFO","PCRYPT_SMART_CARD_ROOT_INFO structure pointer [Security]","security.crypt_smart_card_root_info","wincrypt/CRYPT_SMART_CARD_ROOT_INFO","wincrypt/PCRYPT_SMART_CARD_ROOT_INFO"]
old-location: security\crypt_smart_card_root_info.htm
tech.root: security
ms.assetid: 165a1a9e-e426-4823-8d1b-f13c338964c9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_SMART_CARD_ROOT_INFO, CRYPT_SMART_CARD_ROOT_INFO, CRYPT_SMART_CARD_ROOT_INFO structure [Security], PCRYPT_SMART_CARD_ROOT_INFO, PCRYPT_SMART_CARD_ROOT_INFO structure pointer [Security], security.crypt_smart_card_root_info, wincrypt/CRYPT_SMART_CARD_ROOT_INFO, wincrypt/PCRYPT_SMART_CARD_ROOT_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_SMART_CARD_ROOT_INFO, *PCRYPT_SMART_CARD_ROOT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_SMART_CARD_ROOT_INFO
 - wincrypt/_CRYPT_SMART_CARD_ROOT_INFO
 - PCRYPT_SMART_CARD_ROOT_INFO
 - wincrypt/PCRYPT_SMART_CARD_ROOT_INFO
 - CRYPT_SMART_CARD_ROOT_INFO
 - wincrypt/CRYPT_SMART_CARD_ROOT_INFO
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
 - CRYPT_SMART_CARD_ROOT_INFO
---

# CRYPT_SMART_CARD_ROOT_INFO structure


## -description

The <b>CRYPT_SMART_CARD_ROOT_INFO</b> structure contains the smart card and session IDs associated with a certificate context. The certificate propagation service uses this structure to transfer smart card data between a smart card and a virtual root certificate store on a computer.

## -struct-fields

### -field rgbCardID

An array of bytes that specify the smart card IDs retrieved by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function with the <i>dwParam</i> parameter set to <b>PP_SMARTCARD_GUID</b>.

### -field luid

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-root_info_luid">ROOT_INFO_LUID</a> structure that specifies a session authentication ID from an access token.

## -remarks

The <b>luid</b> member value comes from the <b>AuthenticationId</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a> structure retrieved by calling the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function.

A certificate context can include an array of multiple <b>CRYPT_SMART_CARD_ROOT_INFO</b> structures, one for each <a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>) that the certificate propagation service has added to a root certificate.