---
UID: NS:wsdbase._WSD_SECURITY_SIGNATURE_VALIDATION
title: "_WSD_SECURITY_SIGNATURE_VALIDATION"
author: windows-sdk-content
description: Represents the criteria for matching client compact signatures against messages.
old-location: ncd\wsd_security_signature_validation.htm
tech.root: wsdapi
ms.assetid: e2913f85-a5e7-43c9-a23c-81d836c9a259
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWSD_SECURITY_SIGNATURE_VALIDATION, WSD_SECURITY_SIGNATURE_VALIDATION, WSD_SECURITY_SIGNATURE_VALIDATION structure, _WSD_SECURITY_SIGNATURE_VALIDATION, ncd.wsd_security_signature_validation, wsdbase/WSD_SECURITY_SIGNATURE_VALIDATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wsdbase.h
api_name:
 - WSD_SECURITY_SIGNATURE_VALIDATION
product: Windows
targetos: Windows
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
req.redist: 
---

# _WSD_SECURITY_SIGNATURE_VALIDATION structure


## -description


Represents the criteria for matching client compact signatures against messages.


## -struct-fields




### -field signingCertArray

An array of <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> stuctures that contain certificates to be matched against a message.  Only one matching certificate is required for validatation.  This parameter can be <b>NULL</b>.


### -field dwSigningCertArrayCount

The count of certificates in <i>signingMatchArray</i>.


### -field hSigningCertStore

A handle to a certificate store that contains certificates to be matched against a message.  Only one matching certificate is required for validatation.  This parameter can be <b>NULL</b>.


### -field dwFlags

A flag that specifies how unsigned messages are handled.  If set to <b>WSDAPI_COMPACTSIG_ACCEPT_ALL_MESSAGES</b>, then the discovery object will accept unsigned messages, signed-and-verified messages and signed-but-verified, (that is, those for which the signing cert could not be found either in the store or the certificate  array) messages. If this flag is not set, then only the signed-and-verified messages will be accepted.

If <b>WSDAPI_COMPACTSIG_ACCEPT_ALL_MESSAGES</b> is specified, the caller will not be able use the <a href="https://msdn.microsoft.com/10e95100-4890-4c00-b231-bb7125fed197">IWSDSignatureProperty</a> interface to learn whether the message was signed or not.


## -remarks



This structure is used in the <b>pConfigData</b> member of the <a href="https://msdn.microsoft.com/58dc3e11-586e-4185-b1d0-4249b4bfb252">WSD_CONFIG_PARAM</a> structure when <b>configParamType</b> is set to <b>WSD_SECURITY_COMPACTSIG_VALIDATION</b>.

<b>WSD_SECURITY_SIGNATURE_VALIDATION</b> defines 2 matching mechanisms.  To obtain a match, at least one such mechanism must be satisfied.



