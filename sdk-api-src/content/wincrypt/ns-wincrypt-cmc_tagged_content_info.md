---
UID: NS:wincrypt._CMC_TAGGED_CONTENT_INFO
title: CMC_TAGGED_CONTENT_INFO (wincrypt.h)
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures. (CMC_TAGGED_CONTENT_INFO)
helpviewer_keywords: ["*PCMC_TAGGED_CONTENT_INFO","CMC_TAGGED_CONTENT_INFO","CMC_TAGGED_CONTENT_INFO structure [Security]","PCMC_TAGGED_CONTENT_INFO","PCMC_TAGGED_CONTENT_INFO structure pointer [Security]","_crypto2_cmc_tagged_content_info","security.cmc_tagged_content_info","wincrypt/CMC_TAGGED_CONTENT_INFO","wincrypt/PCMC_TAGGED_CONTENT_INFO"]
old-location: security\cmc_tagged_content_info.htm
tech.root: security
ms.assetid: ff10dcdf-4c76-434a-a8bd-78d64ea24d23
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO structure [Security], PCMC_TAGGED_CONTENT_INFO, PCMC_TAGGED_CONTENT_INFO structure pointer [Security], _crypto2_cmc_tagged_content_info, security.cmc_tagged_content_info, wincrypt/CMC_TAGGED_CONTENT_INFO, wincrypt/PCMC_TAGGED_CONTENT_INFO'
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
req.typenames: CMC_TAGGED_CONTENT_INFO, *PCMC_TAGGED_CONTENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_TAGGED_CONTENT_INFO
 - wincrypt/_CMC_TAGGED_CONTENT_INFO
 - PCMC_TAGGED_CONTENT_INFO
 - wincrypt/PCMC_TAGGED_CONTENT_INFO
 - CMC_TAGGED_CONTENT_INFO
 - wincrypt/CMC_TAGGED_CONTENT_INFO
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
 - CMC_TAGGED_CONTENT_INFO
---

# CMC_TAGGED_CONTENT_INFO structure


## -description

The <b>CMC_TAGGED_CONTENT_INFO</b> structure is used in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_data_info">CMC_DATA_INFO</a> and 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_response_info">CMC_RESPONSE_INFO</a> structures.

## -struct-fields

### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.

### -field EncodedContentInfo

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains the encoded content information.
