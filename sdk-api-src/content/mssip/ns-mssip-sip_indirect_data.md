---
UID: NS:mssip.SIP_INDIRECT_DATA_
title: SIP_INDIRECT_DATA (mssip.h)
description: Contains the digest of the hashed subject information.
helpviewer_keywords: ["*PSIP_INDIRECT_DATA","PSIP_INDIRECT_DATA","PSIP_INDIRECT_DATA structure pointer [Security]","SIP_INDIRECT_DATA","SIP_INDIRECT_DATA structure [Security]","mssip/PSIP_INDIRECT_DATA","mssip/SIP_INDIRECT_DATA","security.sip_indirect_data"]
old-location: security\sip_indirect_data.htm
tech.root: security
ms.assetid: d34b599b-fe49-47c4-bb52-73ee14d73253
ms.date: 12/05/2018
ms.keywords: '*PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA structure pointer [Security], SIP_INDIRECT_DATA, SIP_INDIRECT_DATA structure [Security], mssip/PSIP_INDIRECT_DATA, mssip/SIP_INDIRECT_DATA, security.sip_indirect_data'
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
targetos: Windows
req.typenames: SIP_INDIRECT_DATA, *PSIP_INDIRECT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SIP_INDIRECT_DATA_
 - mssip/SIP_INDIRECT_DATA_
 - PSIP_INDIRECT_DATA
 - mssip/PSIP_INDIRECT_DATA
 - SIP_INDIRECT_DATA
 - mssip/SIP_INDIRECT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_INDIRECT_DATA
---

# SIP_INDIRECT_DATA structure


## -description

The <b>SIP_INDIRECT_DATA</b> structure contains the digest of the hashed subject information.

## -struct-fields

### -field Data

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure used to encode the attribute.

### -field DigestAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the digest algorithm to use to create the <a href="/windows/desktop/SecGloss/h-gly">hash</a>.

### -field Digest

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the hash of the subject. For information about <b>CRYPT_HASH_BLOB</b>, see <b>CRYPT_INTEGER_BLOB</b>.