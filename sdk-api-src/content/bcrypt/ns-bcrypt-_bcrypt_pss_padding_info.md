---
UID: NS:bcrypt._BCRYPT_PSS_PADDING_INFO
title: "_BCRYPT_PSS_PADDING_INFO"
author: windows-sdk-content
description: Used to provide options for the Probabilistic Signature Scheme (PSS) padding scheme.
old-location: security\bcrypt_pss_padding_info.htm
tech.root: seccng
ms.assetid: 28605b34-b1e1-4460-a8f0-b0fe9f9b94d4
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: BCRYPT_PSS_PADDING_INFO, BCRYPT_PSS_PADDING_INFO structure [Security], _BCRYPT_PSS_PADDING_INFO, bcrypt/BCRYPT_PSS_PADDING_INFO, security.bcrypt_pss_padding_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bcrypt.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_PSS_PADDING_INFO
product: Windows
targetos: Windows
req.typenames: BCRYPT_PSS_PADDING_INFO
req.redist: 
---

# _BCRYPT_PSS_PADDING_INFO structure


## -description


The <b>BCRYPT_PSS_PADDING_INFO</b> structure is used to provide options for the Probabilistic Signature Scheme (PSS) padding scheme.


## -struct-fields




### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a>.


### -field cbSalt

The size, in bytes, of the random salt to use for the padding.


## -see-also




<a href="https://msdn.microsoft.com/f402ea9e-89ae-4ccc-9591-aa2328287c0e">BCryptSignHash</a>



<a href="https://msdn.microsoft.com/95c32056-e444-441c-bbc1-c5ae82aba964">BCryptVerifySignature</a>
 

 

