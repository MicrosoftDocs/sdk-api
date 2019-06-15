---
UID: NS:wincrypt._CMC_TAGGED_CONTENT_INFO
title: CMC_TAGGED_CONTENT_INFO (wincrypt.h)
author: windows-sdk-content
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures.
old-location: security\cmc_tagged_content_info.htm
tech.root: SecCrypto
ms.assetid: ff10dcdf-4c76-434a-a8bd-78d64ea24d23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO structure [Security], PCMC_TAGGED_CONTENT_INFO, PCMC_TAGGED_CONTENT_INFO structure pointer [Security], _crypto2_cmc_tagged_content_info, security.cmc_tagged_content_info, wincrypt/CMC_TAGGED_CONTENT_INFO, wincrypt/PCMC_TAGGED_CONTENT_INFO"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMC_TAGGED_CONTENT_INFO
product: Windows
targetos: Windows
req.typenames: CMC_TAGGED_CONTENT_INFO, *PCMC_TAGGED_CONTENT_INFO
req.redist: 
ms.custom: 19H1
---

# CMC_TAGGED_CONTENT_INFO structure


## -description


The <b>CMC_TAGGED_CONTENT_INFO</b> structure is used in the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cmc_data_info">CMC_DATA_INFO</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cmc_response_info">CMC_RESPONSE_INFO</a> structures.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.


### -field EncodedContentInfo

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains the encoded content information.

