---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
title: CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT (cryptuiapi.h)
description: Used with the CryptUIWizDigitalSign function to contain information about a BLOB.
helpviewer_keywords: ["*PCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT","CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT","CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure [Security]","PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT","PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT","cryptuiapi/PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT","security.cryptui_wiz_digital_sign_context"]
old-location: security\cryptui_wiz_digital_sign_context.htm
tech.root: security
ms.assetid: 3e4eb745-0c28-4ce5-870b-d24565ef0cae
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure [Security], PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, cryptuiapi/PCCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, security.cryptui_wiz_digital_sign_context'
req.header: cryptuiapi.h
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
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT, *PCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
 - cryptuiapi/_CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
 - PCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
 - cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
 - CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
 - cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT
---

# CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</b> structure is used with the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a> function to contain information about a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

## -struct-fields

### -field dwSize

The size, in bytes, of the structure.

### -field cbBlob

The size, in bytes, of the BLOB pointed to by the <b>pbBlob</b> member.

### -field pbBlob

A pointer to the signed BLOB.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a>