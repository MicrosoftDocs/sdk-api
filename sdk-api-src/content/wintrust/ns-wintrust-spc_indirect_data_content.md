---
UID: NS:wintrust._SPC_INDIRECT_DATA_CONTENT
title: SPC_INDIRECT_DATA_CONTENT (wintrust.h)

description: Is used in Authenticode signatures to store the digest and other attributes of the signed file.
old-location: security\spc_indirect_data_content.htm
tech.root: SecCrypto
ms.assetid: BD790CA5-9C51-4483-93C1-5492154BF913

ms.date: 12/05/2018
ms.keywords: '*PSPC_INDIRECT_DATA_CONTENT, PSPC_INDIRECT_DATA_CONTENT, PSPC_INDIRECT_DATA_CONTENT structure pointer [Security], SPC_INDIRECT_DATA_CONTENT, SPC_INDIRECT_DATA_CONTENT structure [Security], security.spc_indirect_data_content, wintrust/PSPC_INDIRECT_DATA_CONTENT, wintrust/SPC_INDIRECT_DATA_CONTENT'
ms.topic: struct
f1_keywords:
- wintrust/SPC_INDIRECT_DATA_CONTENT
dev_langs:
 - c++
req.header: wintrust.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wintrust.h
api_name:
- SPC_INDIRECT_DATA_CONTENT
targetos: Windows
req.typenames: SPC_INDIRECT_DATA_CONTENT, *PSPC_INDIRECT_DATA_CONTENT
req.redist: 
ms.custom: 19H1
---

# SPC_INDIRECT_DATA_CONTENT structure


## -description


The <b>SPC_INDIRECT_DATA_CONTENT</b> structure is used in Authenticode signatures to store the digest and other attributes of the signed file.


## -struct-fields




### -field Data

A <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> that contains attributes of the digested file.


### -field DigestAlgorithm

Specifies the digest algorithm used to hash the file.


### -field Digest

The Authenticode digest value of the file using the algorithm specified in the  <i>DigestAlgorithm</i> parameter.

