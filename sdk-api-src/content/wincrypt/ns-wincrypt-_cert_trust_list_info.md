---
UID: NS:wincrypt._CERT_TRUST_LIST_INFO
title: "_CERT_TRUST_LIST_INFO"
author: windows-sdk-content
description: The CERT_TRUST_LIST_INFO structure that indicates valid usage of a CTL.
old-location: security\cert_trust_list_info.htm
old-project: SecCrypto
ms.assetid: 774f5626-9b48-4585-b713-adbf191861cc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PCERT_TRUST_LIST_INFO, CERT_TRUST_LIST_INFO, CERT_TRUST_LIST_INFO structure [Security], PCERT_TRUST_LIST_INFO, PCERT_TRUST_LIST_INFO structure pointer [Security], _CERT_TRUST_LIST_INFO, _crypto2_cert_trust_list_info, security.cert_trust_list_info, wincrypt/CERT_TRUST_LIST_INFO, wincrypt/PCERT_TRUST_LIST_INFO"
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
tech.root: 
req.typenames: CERT_TRUST_LIST_INFO, *PCERT_TRUST_LIST_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_TRUST_LIST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_TRUST_LIST_INFO structure


## -description


The <b>CERT_TRUST_LIST_INFO</b> structure that indicates valid usage of a CTL.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field pCtlEntry

A pointer to a structure that includes a subject identifier, the count of attributes associated with a CTL, and an array of those attributes.


### -field pCtlContext

A pointer to a CTL context.


## -see-also




<a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a>



<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a>
 

 

