---
UID: NS:wsdbase._WSD_SECURITY_SIGNATURE_VALIDATION
title: WSD_SECURITY_SIGNATURE_VALIDATION (wsdbase.h)
description: Represents the criteria for matching client compact signatures against messages.
helpviewer_keywords: ["*PWSD_SECURITY_SIGNATURE_VALIDATION","WSD_SECURITY_SIGNATURE_VALIDATION","WSD_SECURITY_SIGNATURE_VALIDATION structure","_WSD_SECURITY_SIGNATURE_VALIDATION","ncd.wsd_security_signature_validation","wsdbase/WSD_SECURITY_SIGNATURE_VALIDATION"]
old-location: ncd\wsd_security_signature_validation.htm
tech.root: ncd
ms.assetid: e2913f85-a5e7-43c9-a23c-81d836c9a259
ms.date: 12/05/2018
ms.keywords: '*PWSD_SECURITY_SIGNATURE_VALIDATION, WSD_SECURITY_SIGNATURE_VALIDATION, WSD_SECURITY_SIGNATURE_VALIDATION structure, _WSD_SECURITY_SIGNATURE_VALIDATION, ncd.wsd_security_signature_validation, wsdbase/WSD_SECURITY_SIGNATURE_VALIDATION'
req.header: wsdbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SECURITY_SIGNATURE_VALIDATION
 - wsdbase/_WSD_SECURITY_SIGNATURE_VALIDATION
 - PWSD_SECURITY_SIGNATURE_VALIDATION
 - wsdbase/PWSD_SECURITY_SIGNATURE_VALIDATION
 - WSD_SECURITY_SIGNATURE_VALIDATION
 - wsdbase/WSD_SECURITY_SIGNATURE_VALIDATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wsdbase.h
api_name:
 - WSD_SECURITY_SIGNATURE_VALIDATION
---

# WSD_SECURITY_SIGNATURE_VALIDATION structure


## -description

Represents the criteria for matching client compact signatures against messages.

## -struct-fields

### -field signingCertArray

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> stuctures that contain certificates to be matched against a message.  Only one matching certificate is required for validation.  This parameter can be <b>NULL</b>.

### -field dwSigningCertArrayCount

The count of certificates in <i>signingMatchArray</i>.

### -field hSigningCertStore

A handle to a certificate store that contains certificates to be matched against a message.  Only one matching certificate is required for validation.  This parameter can be <b>NULL</b>.

### -field dwFlags

A flag that specifies how unsigned messages are handled.  If set to <b>WSDAPI_COMPACTSIG_ACCEPT_ALL_MESSAGES</b>, then the discovery object will accept unsigned messages, signed-and-verified messages and signed-but-verified, (that is, those for which the signing cert could not be found either in the store or the certificate  array) messages. If this flag is not set, then only the signed-and-verified messages will be accepted.

If <b>WSDAPI_COMPACTSIG_ACCEPT_ALL_MESSAGES</b> is specified, the caller will not be able use the <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdsignatureproperty">IWSDSignatureProperty</a> interface to learn whether the message was signed or not.

## -remarks

This structure is used in the <b>pConfigData</b> member of the <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> structure when <b>configParamType</b> is set to <b>WSD_SECURITY_COMPACTSIG_VALIDATION</b>.

<b>WSD_SECURITY_SIGNATURE_VALIDATION</b> defines 2 matching mechanisms.  To obtain a match, at least one such mechanism must be satisfied.