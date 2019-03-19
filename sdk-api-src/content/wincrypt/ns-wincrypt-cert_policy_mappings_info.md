---
UID: NS:wincrypt._CERT_POLICY_MAPPINGS_INFO
title: CERT_POLICY_MAPPINGS_INFO (wincrypt.h)
author: windows-sdk-content
description: The CERT_POLICY_MAPPINGS_INFO structure provides mapping between the policy OIDs of two domains.
old-location: security\cert_policy_mappings_info.htm
tech.root: SecCrypto
ms.assetid: dcc44691-d621-4e28-8618-38238f866302
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_POLICY_MAPPINGS_INFO, CERT_POLICY_MAPPINGS_INFO, CERT_POLICY_MAPPINGS_INFO structure [Security], PCERT_POLICY_MAPPINGS_INFO, PCERT_POLICY_MAPPINGS_INFO structure pointer [Security], _crypto2_cert_policy_mappings_info, security.cert_policy_mappings_info, wincrypt/CERT_POLICY_MAPPINGS_INFO, wincrypt/PCERT_POLICY_MAPPINGS_INFO"
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
 - CERT_POLICY_MAPPINGS_INFO
product: Windows
targetos: Windows
req.typenames: CERT_POLICY_MAPPINGS_INFO, *PCERT_POLICY_MAPPINGS_INFO
req.redist: 
---

# CERT_POLICY_MAPPINGS_INFO structure


## -description


The <b>CERT_POLICY_MAPPINGS_INFO</b> structure provides mapping between the policy OIDs of two domains.


## -struct-fields




### -field cPolicyMapping

Count of the number of elements in the <b>rgPolicyMapping</b> array.


### -field rgPolicyMapping

Array of 
<a href="https://msdn.microsoft.com/6270888a-1c61-472d-8ec7-10c24b890220">CERT_POLICY_MAPPING</a> structures. Each element of this array provides pair of OIDs mapping the identifies of one domain to identifiers in the other domain.

