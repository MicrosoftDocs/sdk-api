---
UID: NS:wincrypt._CMC_RESPONSE_INFO
title: CMC_RESPONSE_INFO (wincrypt.h)
description: Provides a means of communicating different pieces of tagged information. (CMC_RESPONSE_INFO)
helpviewer_keywords: ["*PCMC_RESPONSE_INFO","CMC_RESPONSE_INFO","CMC_RESPONSE_INFO structure [Security]","PCMC_RESPONSE_INFO","PCMC_RESPONSE_INFO structure pointer [Security]","_crypto2_cmc_response_info","security.cmc_response_info","wincrypt/CMC_RESPONSE_INFO","wincrypt/PCMC_RESPONSE_INFO"]
old-location: security\cmc_response_info.htm
tech.root: security
ms.assetid: 82d9314f-2f0f-4a98-a0da-a89cd8905886
ms.date: 12/05/2018
ms.keywords: '*PCMC_RESPONSE_INFO, CMC_RESPONSE_INFO, CMC_RESPONSE_INFO structure [Security], PCMC_RESPONSE_INFO, PCMC_RESPONSE_INFO structure pointer [Security], _crypto2_cmc_response_info, security.cmc_response_info, wincrypt/CMC_RESPONSE_INFO, wincrypt/PCMC_RESPONSE_INFO'
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
req.typenames: CMC_RESPONSE_INFO, *PCMC_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_RESPONSE_INFO
 - wincrypt/_CMC_RESPONSE_INFO
 - PCMC_RESPONSE_INFO
 - wincrypt/PCMC_RESPONSE_INFO
 - CMC_RESPONSE_INFO
 - wincrypt/CMC_RESPONSE_INFO
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
 - CMC_RESPONSE_INFO
---

# CMC_RESPONSE_INFO structure


## -description

The <b>CMC_RESPONSE_INFO</b> structure provides a means of communicating different pieces of tagged information.

## -struct-fields

### -field cTaggedAttribute

Count of the number of elements in the <b>rgTaggedAttribute</b> member array.

### -field rgTaggedAttribute

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_attribute">CMC_TAGGED_ATTRIBUTE</a> structures.

### -field cTaggedContentInfo

Count of the number of elements in the <b>rgTaggedContentInfo</b> member array.

### -field rgTaggedContentInfo

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_content_info">CMC_TAGGED_CONTENT_INFO</a> structures.

### -field cTaggedOtherMsg

Count of the number of elements in the <b>rgTaggedOtherMsg</b> member array.

### -field rgTaggedOtherMsg

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_other_msg">CMC_TAGGED_OTHER_MSG</a> structures.

## -remarks

All tagged arrays are optional.
