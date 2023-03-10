---
UID: NS:wincrypt._CMC_TAGGED_OTHER_MSG
title: CMC_TAGGED_OTHER_MSG (wincrypt.h)
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures. (CMC_TAGGED_OTHER_MSG)
helpviewer_keywords: ["*PCMC_TAGGED_OTHER_MSG","CMC_TAGGED_OTHER_MSG","CMC_TAGGED_OTHER_MSG structure [Security]","PCMC_TAGGED_OTHER_MSG","PCMC_TAGGED_OTHER_MSG structure pointer [Security]","_crypto2_cmc_tagged_other_msg","security.cmc_tagged_other_msg","wincrypt/CMC_TAGGED_OTHER_MSG","wincrypt/PCMC_TAGGED_OTHER_MSG"]
old-location: security\cmc_tagged_other_msg.htm
tech.root: security
ms.assetid: cf70c245-fe22-4c02-9cfd-07690b930585
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_OTHER_MSG, CMC_TAGGED_OTHER_MSG, CMC_TAGGED_OTHER_MSG structure [Security], PCMC_TAGGED_OTHER_MSG, PCMC_TAGGED_OTHER_MSG structure pointer [Security], _crypto2_cmc_tagged_other_msg, security.cmc_tagged_other_msg, wincrypt/CMC_TAGGED_OTHER_MSG, wincrypt/PCMC_TAGGED_OTHER_MSG'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CMC_TAGGED_OTHER_MSG, *PCMC_TAGGED_OTHER_MSG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_TAGGED_OTHER_MSG
 - wincrypt/_CMC_TAGGED_OTHER_MSG
 - PCMC_TAGGED_OTHER_MSG
 - wincrypt/PCMC_TAGGED_OTHER_MSG
 - CMC_TAGGED_OTHER_MSG
 - wincrypt/CMC_TAGGED_OTHER_MSG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMC_TAGGED_OTHER_MSG
---

# CMC_TAGGED_OTHER_MSG structure


## -description

The <b>CMC_TAGGED_OTHER_MSG</b> structure is used in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_data_info">CMC_DATA_INFO</a> and 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_response_info">CMC_RESPONSE_INFO</a> structures.

## -struct-fields

### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.

### -field pszObjId

Object identifier (OID) of the other message.

### -field Value

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> structure that contains the encoded other message information.
