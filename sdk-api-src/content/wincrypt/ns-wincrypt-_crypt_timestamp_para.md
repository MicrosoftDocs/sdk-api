---
UID: NS:wincrypt._CRYPT_TIMESTAMP_PARA
title: "_CRYPT_TIMESTAMP_PARA"
author: windows-sdk-content
description: Defines additional parameters for the time stamp request.
old-location: security\crypt_timestamp_para.htm
tech.root: SecCrypto
ms.assetid: 26a6e9d3-b35e-47ae-9cea-a37ca6297c28
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCRYPT_TIMESTAMP_PARA, CRYPT_TIMESTAMP_PARA, CRYPT_TIMESTAMP_PARA structure [Security], PCRYPT_TIMESTAMP_PARA, PCRYPT_TIMESTAMP_PARA structure pointer [Security], _CRYPT_TIMESTAMP_PARA, security.crypt_timestamp_para, wincrypt/CRYPT_TIMESTAMP_PARA, wincrypt/PCRYPT_TIMESTAMP_PARA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
 - Wincrypt.h
api_name:
 - CRYPT_TIMESTAMP_PARA
product: Windows
targetos: Windows
req.typenames: CRYPT_TIMESTAMP_PARA, *PCRYPT_TIMESTAMP_PARA
req.redist: 
---

# _CRYPT_TIMESTAMP_PARA structure


## -description


The <b>CRYPT_TIMESTAMP_PARA</b> structure defines additional parameters for the time stamp request.


## -struct-fields




### -field pszTSAPolicyId

Optional. A pointer to a null-terminated character string that contains the Time Stamping Authority (TSA) policy under which the time stamp token
should be provided.


### -field fRequestCerts

A Boolean value that specifies whether the TSA must include the certificates
used to sign the time stamp token in the response .


### -field Nonce

Optional. A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available.


### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.


### -field rgExtension

A pointer to an array of <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures that contain extension information that is passed in the request.

