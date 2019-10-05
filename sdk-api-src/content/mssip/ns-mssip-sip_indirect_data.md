---
UID: NS:mssip.SIP_INDIRECT_DATA_
title: SIP_INDIRECT_DATA (mssip.h)
author: windows-sdk-content
description: Contains the digest of the hashed subject information.
old-location: security\sip_indirect_data.htm
tech.root: SecCrypto
ms.assetid: d34b599b-fe49-47c4-bb52-73ee14d73253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA structure pointer [Security], SIP_INDIRECT_DATA, SIP_INDIRECT_DATA structure [Security], mssip/PSIP_INDIRECT_DATA, mssip/SIP_INDIRECT_DATA, security.sip_indirect_data'
ms.topic: struct
f1_keywords:
- mssip/SIP_INDIRECT_DATA
dev_langs:
 - c++
req.header: mssip.h
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
- Mssip.h
api_name:
- SIP_INDIRECT_DATA
targetos: Windows
req.typenames: SIP_INDIRECT_DATA, *PSIP_INDIRECT_DATA
req.redist: 
ms.custom: 19H1
---

# SIP_INDIRECT_DATA structure


## -description


The <b>SIP_INDIRECT_DATA</b> structure contains the digest of the hashed subject information.


## -struct-fields




### -field Data

A <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure used to encode the attribute.


### -field DigestAlgorithm

A <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the digest algorithm to use to create the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash</a>.


### -field Digest

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the hash of the subject. For information about <b>CRYPT_HASH_BLOB</b>, see <b>CRYPT_INTEGER_BLOB</b>.

