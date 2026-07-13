---
UID: NS:wincrypt._CMC_TAGGED_ATTRIBUTE
title: CMC_TAGGED_ATTRIBUTE (wincrypt.h)
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures. (CMC_TAGGED_ATTRIBUTE)
helpviewer_keywords: ["*PCMC_TAGGED_ATTRIBUTE","CMC_TAGGED_ATTRIBUTE","CMC_TAGGED_ATTRIBUTE structure [Security]","PCMC_TAGGED_ATTRIBUTE","PCMC_TAGGED_ATTRIBUTE structure pointer [Security]","_crypto2_cmc_tagged_attribute","security.cmc_tagged_attribute","wincrypt/CMC_TAGGED_ATTRIBUTE","wincrypt/PCMC_TAGGED_ATTRIBUTE"]
old-location: security\cmc_tagged_attribute.htm
tech.root: security
ms.assetid: 4c350cda-2318-49b2-86dc-452423ceb9e3
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_ATTRIBUTE, CMC_TAGGED_ATTRIBUTE, CMC_TAGGED_ATTRIBUTE structure [Security], PCMC_TAGGED_ATTRIBUTE, PCMC_TAGGED_ATTRIBUTE structure pointer [Security], _crypto2_cmc_tagged_attribute, security.cmc_tagged_attribute, wincrypt/CMC_TAGGED_ATTRIBUTE, wincrypt/PCMC_TAGGED_ATTRIBUTE'
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
req.typenames: CMC_TAGGED_ATTRIBUTE, *PCMC_TAGGED_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_TAGGED_ATTRIBUTE
 - wincrypt/_CMC_TAGGED_ATTRIBUTE
 - PCMC_TAGGED_ATTRIBUTE
 - wincrypt/PCMC_TAGGED_ATTRIBUTE
 - CMC_TAGGED_ATTRIBUTE
 - wincrypt/CMC_TAGGED_ATTRIBUTE
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
 - CMC_TAGGED_ATTRIBUTE
---

# CMC_TAGGED_ATTRIBUTE structure


## -description

The <b>CMC_TAGGED_ATTRIBUTE</b> structure is used in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_data_info">CMC_DATA_INFO</a> and 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_response_info">CMC_RESPONSE_INFO</a> structures.

## -struct-fields

### -field dwBodyPartID

A <b>DWORD</b> value that identifies the tagged attribute.

### -field Attribute

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structure that contains the attribute.
