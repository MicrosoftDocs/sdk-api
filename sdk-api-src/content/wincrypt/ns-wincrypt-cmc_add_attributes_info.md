---
UID: NS:wincrypt._CMC_ADD_ATTRIBUTES_INFO
title: CMC_ADD_ATTRIBUTES_INFO (wincrypt.h)
description: Contains certificate attributes to be added to a certificate.
helpviewer_keywords: ["*PCMC_ADD_ATTRIBUTES_INFO","CMC_ADD_ATTRIBUTES_INFO","CMC_ADD_ATTRIBUTES_INFO structure [Security]","PCMC_ADD_ATTRIBUTES_INFO","PCMC_ADD_ATTRIBUTES_INFO structure pointer [Security]","_crypto2_cmc_add_attributes_info","security.cmc_add_attributes_info","wincrypt/CMC_ADD_ATTRIBUTES_INFO","wincrypt/PCMC_ADD_ATTRIBUTES_INFO"]
old-location: security\cmc_add_attributes_info.htm
tech.root: security
ms.assetid: fd13cd2b-b818-41ca-85be-d51b864194df
ms.date: 12/05/2018
ms.keywords: '*PCMC_ADD_ATTRIBUTES_INFO, CMC_ADD_ATTRIBUTES_INFO, CMC_ADD_ATTRIBUTES_INFO structure [Security], PCMC_ADD_ATTRIBUTES_INFO, PCMC_ADD_ATTRIBUTES_INFO structure pointer [Security], _crypto2_cmc_add_attributes_info, security.cmc_add_attributes_info, wincrypt/CMC_ADD_ATTRIBUTES_INFO, wincrypt/PCMC_ADD_ATTRIBUTES_INFO'
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
req.typenames: CMC_ADD_ATTRIBUTES_INFO, *PCMC_ADD_ATTRIBUTES_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_ADD_ATTRIBUTES_INFO
 - wincrypt/_CMC_ADD_ATTRIBUTES_INFO
 - PCMC_ADD_ATTRIBUTES_INFO
 - wincrypt/PCMC_ADD_ATTRIBUTES_INFO
 - CMC_ADD_ATTRIBUTES_INFO
 - wincrypt/CMC_ADD_ATTRIBUTES_INFO
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
 - CMC_ADD_ATTRIBUTES_INFO
---

# CMC_ADD_ATTRIBUTES_INFO structure


## -description

The <b>CMC_ADD_ATTRIBUTES_INFO</b> structure contains certificate attributes to be added to a certificate.

## -struct-fields

### -field dwCmcDataReference

<b>DWORD</b> data reference number.

### -field cCertReference

Count of elements in the <b>rgdwCertReference</b> array.

### -field rgdwCertReference

Array of certificate reference numbers.

### -field cAttribute

Count of the elements in the <b>rgAttribute</b> array.

### -field rgAttribute

Array of pointers to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> certificate attributes to be added.