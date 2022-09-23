---
UID: NS:wincrypt._CMC_DATA_INFO
title: CMC_DATA_INFO (wincrypt.h)
description: Provides a means of communicating different pieces of tagged information. (CMC_DATA_INFO)
helpviewer_keywords: ["*PCMC_DATA_INFO","CMC_DATA_INFO","CMC_DATA_INFO structure [Security]","PCMC_DATA_INFO","PCMC_DATA_INFO structure pointer [Security]","_crypto2_cmc_data_info","security.cmc_data_info","wincrypt/CMC_DATA_INFO","wincrypt/PCMC_DATA_INFO"]
old-location: security\cmc_data_info.htm
tech.root: security
ms.assetid: 6245af5a-7a19-4665-bf6c-ad803998d840
ms.date: 12/05/2018
ms.keywords: '*PCMC_DATA_INFO, CMC_DATA_INFO, CMC_DATA_INFO structure [Security], PCMC_DATA_INFO, PCMC_DATA_INFO structure pointer [Security], _crypto2_cmc_data_info, security.cmc_data_info, wincrypt/CMC_DATA_INFO, wincrypt/PCMC_DATA_INFO'
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
req.typenames: CMC_DATA_INFO, *PCMC_DATA_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_DATA_INFO
 - wincrypt/_CMC_DATA_INFO
 - PCMC_DATA_INFO
 - wincrypt/PCMC_DATA_INFO
 - CMC_DATA_INFO
 - wincrypt/CMC_DATA_INFO
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
 - CMC_DATA_INFO
---

# CMC_DATA_INFO structure


## -description

The <b>CMC_DATA_INFO</b> structure provides a means of communicating different pieces of tagged information.

## -struct-fields

### -field cTaggedAttribute

Count of the number of elements in the <b>rgTaggedAttribute</b> member array.

### -field rgTaggedAttribute

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_attribute">CMC_TAGGED_ATTRIBUTE</a> structures.

### -field cTaggedRequest

Count of the number of elements in the <b>rgTaggedRequest</b> member array.

### -field rgTaggedRequest

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_request">CMC_TAGGED_REQUEST</a> structures.

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
