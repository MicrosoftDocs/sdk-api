---
UID: NS:wincrypt._CMC_TAGGED_ATTRIBUTE
title: "_CMC_TAGGED_ATTRIBUTE"
author: windows-sdk-content
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures.
old-location: security\cmc_tagged_attribute.htm
tech.root: seccrypto
ms.assetid: 4c350cda-2318-49b2-86dc-452423ceb9e3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCMC_TAGGED_ATTRIBUTE, CMC_TAGGED_ATTRIBUTE, CMC_TAGGED_ATTRIBUTE structure [Security], PCMC_TAGGED_ATTRIBUTE, PCMC_TAGGED_ATTRIBUTE structure pointer [Security], _CMC_TAGGED_ATTRIBUTE, _crypto2_cmc_tagged_attribute, security.cmc_tagged_attribute, wincrypt/CMC_TAGGED_ATTRIBUTE, wincrypt/PCMC_TAGGED_ATTRIBUTE"
ms.prod: windows
ms.technology: windows-sdk
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
 - CMC_TAGGED_ATTRIBUTE
product: Windows
targetos: Windows
req.typenames: CMC_TAGGED_ATTRIBUTE, *PCMC_TAGGED_ATTRIBUTE
req.redist: 
---

# _CMC_TAGGED_ATTRIBUTE structure


## -description


The <b>CMC_TAGGED_ATTRIBUTE</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> and 
<a href="https://msdn.microsoft.com/82d9314f-2f0f-4a98-a0da-a89cd8905886">CMC_RESPONSE_INFO</a> structures.


## -struct-fields




### -field dwBodyPartID

A <b>DWORD</b> value that identifies the tagged attribute.


### -field Attribute

A <a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structure that contains the attribute.

