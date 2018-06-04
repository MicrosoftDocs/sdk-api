---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



