---
UID: NS:bcrypt._BCRYPT_PSS_PADDING_INFO
title: BCRYPT_PSS_PADDING_INFO (bcrypt.h)
description: Used to provide options for the Probabilistic Signature Scheme (PSS) padding scheme.
helpviewer_keywords: ["BCRYPT_PSS_PADDING_INFO","BCRYPT_PSS_PADDING_INFO structure [Security]","bcrypt/BCRYPT_PSS_PADDING_INFO","security.bcrypt_pss_padding_info"]
old-location: security\bcrypt_pss_padding_info.htm
tech.root: security
ms.assetid: 28605b34-b1e1-4460-a8f0-b0fe9f9b94d4
ms.date: 12/05/2018
ms.keywords: BCRYPT_PSS_PADDING_INFO, BCRYPT_PSS_PADDING_INFO structure [Security], bcrypt/BCRYPT_PSS_PADDING_INFO, security.bcrypt_pss_padding_info
f1_keywords:
- bcrypt/BCRYPT_PSS_PADDING_INFO
dev_langs:
- c++
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
targetos: Windows
req.typenames: BCRYPT_PSS_PADDING_INFO
req.redist: 
ms.custom: 19H1
---

# BCRYPT_PSS_PADDING_INFO structure


## -description


The <b>BCRYPT_PSS_PADDING_INFO</b> structure is used to provide options for the Probabilistic Signature Scheme (PSS) padding scheme.


## -struct-fields




### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hashing algorithm</a>.


### -field cbSalt

The size, in bytes, of the random salt to use for the padding.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptverifysignature">BCryptVerifySignature</a>
 

 

