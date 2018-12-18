---
UID: NS:wincrypt._CMC_RESPONSE_INFO
title: CMC_RESPONSE_INFO
author: windows-sdk-content
description: Provides a means of communicating different pieces of tagged information.
old-location: security\cmc_response_info.htm
tech.root: seccrypto
ms.assetid: 82d9314f-2f0f-4a98-a0da-a89cd8905886
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCMC_RESPONSE_INFO, CMC_RESPONSE_INFO, CMC_RESPONSE_INFO structure [Security], PCMC_RESPONSE_INFO, PCMC_RESPONSE_INFO structure pointer [Security], _crypto2_cmc_response_info, security.cmc_response_info, wincrypt/CMC_RESPONSE_INFO, wincrypt/PCMC_RESPONSE_INFO"
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
 - CMC_RESPONSE_INFO
product: Windows
targetos: Windows
req.typenames: CMC_RESPONSE_INFO, *PCMC_RESPONSE_INFO
req.redist: 
---

# CMC_RESPONSE_INFO structure


## -description


The <b>CMC_RESPONSE_INFO</b> structure provides a means of communicating different pieces of tagged information.


## -struct-fields




### -field cTaggedAttribute

Count of the number of elements in the <b>rgTaggedAttribute</b> member array.


### -field rgTaggedAttribute

Array of 
<a href="https://msdn.microsoft.com/4c350cda-2318-49b2-86dc-452423ceb9e3">CMC_TAGGED_ATTRIBUTE</a> structures.


### -field cTaggedContentInfo

Count of the number of elements in the <b>rgTaggedContentInfo</b> member array.


### -field rgTaggedContentInfo

Array of 
<a href="https://msdn.microsoft.com/ff10dcdf-4c76-434a-a8bd-78d64ea24d23">CMC_TAGGED_CONTENT_INFO</a> structures.


### -field cTaggedOtherMsg

Count of the number of elements in the <b>rgTaggedOtherMsg</b> member array.


### -field rgTaggedOtherMsg

Array of 
<a href="https://msdn.microsoft.com/cf70c245-fe22-4c02-9cfd-07690b930585">CMC_TAGGED_OTHER_MSG</a> structures.


## -remarks



All tagged arrays are optional.



