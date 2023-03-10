---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
title: CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO (cryptuiapi.h)
description: Contains information about the certificate store used by the digital signature wizard.
helpviewer_keywords: ["*PCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO","CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO","CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure [Security]","PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO","PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO","cryptuiapi/PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO","security.cryptui_wiz_digital_sign_store_info"]
old-location: security\cryptui_wiz_digital_sign_store_info.htm
tech.root: security
ms.assetid: d3ffbf1c-e8c2-44ab-84d2-d32350d04407
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure [Security], PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, cryptuiapi/PCCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, security.cryptui_wiz_digital_sign_store_info'
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
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
 - cryptuiapi/_CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
 - PCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
 - cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
 - CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
 - cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
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
 - CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO
---

# CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</b> structure contains information about the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> used by the digital signature wizard.

## -struct-fields

### -field dwSize

The size, in bytes, of the structure. This value must be set to <code>sizeof(CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO)</code>.

### -field cCertStore

Number of certificates in the <b>rghCertStore</b> member.

### -field rghCertStore

A pointer to a handle to the certificate store that will be used by the digital signature wizard.

### -field pFilterCallback

Filter callback function used to display the certificate.

### -field pvCallbackData

A pointer to the callback data.