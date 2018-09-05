---
UID: NS:wincrypt._CERT_X942_DH_VALIDATION_PARAMS
title: "_CERT_X942_DH_VALIDATION_PARAMS"
author: windows-sdk-content
description: Optionally pointed to by a member of the CERT_X942_DH_PARAMETERS structure and contains additional seed information.
old-location: security\cert_x942_dh_validation_params.htm
old-project: seccrypto
ms.assetid: 26c367d5-c338-4db3-9973-ce21dcddf7ca
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCERT_X942_DH_VALIDATION_PARAMS, CERT_942_DH_VALIDATION_PARAMS, CERT_942_DH_VALIDATION_PARAMS structure [Security], CERT_X942_DH_VALIDATION_PARAMS, CERT_X942_DH_VALIDATION_PARAMS structure [Security], PCERT942_DH_VALIDATION_PARAMS, PCERT942_DH_VALIDATION_PARAMS structure pointer [Security], _CERT_X942_DH_VALIDATION_PARAMS, _crypto2_cert_x942_dh_validation_params, security.cert_x942_dh_validation_params, wincrypt/CERT_X942_DH_VALIDATION_PARAMS, wincrypt/PCERT942_DH_VALIDATION_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
req.typenames: CERT_X942_DH_VALIDATION_PARAMS, *PCERT_X942_DH_VALIDATION_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_942_DH_VALIDATION_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_X942_DH_VALIDATION_PARAMS structure


## -description


The <b>CERT_X942_DH_VALIDATION_PARAMS</b> structure is optionally pointed to by a member of the <a href="https://msdn.microsoft.com/833d8e36-af78-4daa-92c5-0cb37a31df2f">CERT_X942_DH_PARAMETERS</a> structure and contains additional seed information.


## -struct-fields




### -field seed

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_UINT_BLOB</a> that contains an unsigned seed value.


### -field pgenCounter

A <b>DWORD</b> counter.

