---
UID: NS:wincrypt._CMC_DATA_INFO
title: "_CMC_DATA_INFO"
author: windows-driver-content
description: Provides a means of communicating different pieces of tagged information.
old-location: security\cmc_data_info.htm
old-project: SecCrypto
ms.assetid: 6245af5a-7a19-4665-bf6c-ad803998d840
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PCMC_DATA_INFO, CMC_DATA_INFO, CMC_DATA_INFO structure [Security], PCMC_DATA_INFO, PCMC_DATA_INFO structure pointer [Security], _CMC_DATA_INFO, _crypto2_cmc_data_info, security.cmc_data_info, wincrypt/CMC_DATA_INFO, wincrypt/PCMC_DATA_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CMC_DATA_INFO, *PCMC_DATA_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMC_DATA_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMC_DATA_INFO structure


## -description


The <b>CMC_DATA_INFO</b> structure provides a means of communicating different pieces of tagged information.


## -struct-fields




### -field cTaggedAttribute

Count of the number of elements in the <b>rgTaggedAttribute</b> member array.


### -field rgTaggedAttribute

Array of 
<a href="https://msdn.microsoft.com/4c350cda-2318-49b2-86dc-452423ceb9e3">CMC_TAGGED_ATTRIBUTE</a> structures.


### -field cTaggedRequest

Count of the number of elements in the <b>rgTaggedRequest</b> member array.


### -field rgTaggedRequest

Array of 
<a href="https://msdn.microsoft.com/425a3f14-8bc9-471d-b11c-1608db473cce">CMC_TAGGED_REQUEST</a> structures.


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



