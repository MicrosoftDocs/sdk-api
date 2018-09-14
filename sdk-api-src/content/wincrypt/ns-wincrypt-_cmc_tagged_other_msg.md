---
UID: NS:wincrypt._CMC_TAGGED_OTHER_MSG
title: "_CMC_TAGGED_OTHER_MSG"
author: windows-sdk-content
description: Used in the CMC_DATA_INFO and CMC_RESPONSE_INFO structures.
old-location: security\cmc_tagged_other_msg.htm
tech.root: seccrypto
ms.assetid: cf70c245-fe22-4c02-9cfd-07690b930585
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCMC_TAGGED_OTHER_MSG, CMC_TAGGED_OTHER_MSG, CMC_TAGGED_OTHER_MSG structure [Security], PCMC_TAGGED_OTHER_MSG, PCMC_TAGGED_OTHER_MSG structure pointer [Security], _CMC_TAGGED_OTHER_MSG, _crypto2_cmc_tagged_other_msg, security.cmc_tagged_other_msg, wincrypt/CMC_TAGGED_OTHER_MSG, wincrypt/PCMC_TAGGED_OTHER_MSG"
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
 - CMC_TAGGED_OTHER_MSG
product: Windows
targetos: Windows
req.typenames: CMC_TAGGED_OTHER_MSG, *PCMC_TAGGED_OTHER_MSG
req.redist: 
---

# _CMC_TAGGED_OTHER_MSG structure


## -description


The <b>CMC_TAGGED_OTHER_MSG</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> and 
<a href="https://msdn.microsoft.com/82d9314f-2f0f-4a98-a0da-a89cd8905886">CMC_RESPONSE_INFO</a> structures.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.


### -field pszObjId

Object identifier (OID) of the other message.


### -field Value

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains the encoded other message information.

