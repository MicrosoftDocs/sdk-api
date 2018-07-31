---
UID: NS:wincrypt._CERT_X942_DH_PARAMETERS
title: "_CERT_X942_DH_PARAMETERS"
author: windows-sdk-content
description: Contains parameters associated with a Diffie-Hellman public key algorithm.
old-location: security\cert_x942_dh_parameters.htm
old-project: SecCrypto
ms.assetid: 833d8e36-af78-4daa-92c5-0cb37a31df2f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PCERT_X942_DH_PARAMETERS, CERT_X942_DH_PARAMETERS, CERT_X942_DH_PARAMETERS structure [Security], PCERT_X942_DH_PARAMETERS, PCERT_X942_DH_PARAMETERS structure pointer [Security], _CERT_X942_DH_PARAMETERS, _crypto2_cert_x942_dh_parameters, security.cert_x942_dh_parameters, wincrypt/CERT_X942_DH_PARAMETERS, wincrypt/PCERT_X942_DH_PARAMETERS"
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
req.typenames: CERT_X942_DH_PARAMETERS, *PCERT_X942_DH_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_X942_DH_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_X942_DH_PARAMETERS structure


## -description


The <b>CERT_X942_DH_PARAMETERS</b> structure contains parameters associated with a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a>.


## -struct-fields




### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.


### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).


### -field q

Prime Q. 




A factor of p–1. The most significant bit of the most significant byte must be set to 1.


### -field j

Optional subgroup factor.


### -field pValidationParams

Optional pointer to a <a href="https://msdn.microsoft.com/26c367d5-c338-4db3-9973-ce21dcddf7ca">CERT_X942_DH_VALIDATION_PARAMS</a> structure. If the <b>cbData</b> member of the q BLOB is zero, all of the members of <b>pValidationParams</b> must be zero.

