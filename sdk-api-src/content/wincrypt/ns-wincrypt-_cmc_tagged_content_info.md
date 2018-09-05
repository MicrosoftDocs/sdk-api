---
UID: NS:wincrypt._CMC_TAGGED_CONTENT_INFO
title: "_CMC_TAGGED_CONTENT_INFO"
author: windows-sdk-content
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures.
old-location: security\cmc_tagged_content_info.htm
old-project: seccrypto
ms.assetid: ff10dcdf-4c76-434a-a8bd-78d64ea24d23
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO, CMC_TAGGED_CONTENT_INFO structure [Security], PCMC_TAGGED_CONTENT_INFO, PCMC_TAGGED_CONTENT_INFO structure pointer [Security], _CMC_TAGGED_CONTENT_INFO, _crypto2_cmc_tagged_content_info, security.cmc_tagged_content_info, wincrypt/CMC_TAGGED_CONTENT_INFO, wincrypt/PCMC_TAGGED_CONTENT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CMC_TAGGED_CONTENT_INFO, *PCMC_TAGGED_CONTENT_INFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMC_TAGGED_CONTENT_INFO structure


## -description


The <b>CMC_TAGGED_CONTENT_INFO</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> and 
<a href="https://msdn.microsoft.com/82d9314f-2f0f-4a98-a0da-a89cd8905886">CMC_RESPONSE_INFO</a> structures.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.


### -field EncodedContentInfo

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains the encoded content information.

