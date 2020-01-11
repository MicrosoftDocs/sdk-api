---
UID: NS:ipsectypes.IPSEC_ID0_
title: IPSEC_ID0 (ipsectypes.h)
description: Contains information corresponding to identities that are authenticated by IPsec.
old-location: fwp\ipsec_id0.htm
tech.root: fwp
ms.assetid: e8881c50-9586-447e-a514-cc28895e5e90
ms.date: 12/05/2018
ms.keywords: IPSEC_ID0, IPSEC_ID0 structure [Filtering], fwp.ipsec_id0, ipsectypes/IPSEC_ID0
f1_keywords:
- ipsectypes/IPSEC_ID0
dev_langs:
- c++
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
- Ipsectypes.h
api_name:
- IPSEC_ID0
targetos: Windows
req.typenames: IPSEC_ID0
req.redist: 
ms.custom: 19H1
---

# IPSEC_ID0 structure


## -description


The <b>IPSEC_ID0</b> structure  contains information corresponding to identities that are authenticated by IPsec.


## -struct-fields




### -field mmTargetName

Optional main mode target service principal name (SPN).  This is often the machine name.


### -field emTargetName

Optional extended mode target SPN.


### -field numTokens

Optional.  Number of [IPSEC_TOKEN0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_token0)a> structures present in the <b>tokens</b> member.


### -field tokens

Optional array of [IPSEC_TOKEN0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_token0)a> structures.


### -field explicitCredentials

Optional handle to explicit credentials.


### -field logonId

Unused parameter. This should always be 0.


## -remarks



<b>IPSEC_ID0</b> is a specific implementation of IPSEC_ID. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

