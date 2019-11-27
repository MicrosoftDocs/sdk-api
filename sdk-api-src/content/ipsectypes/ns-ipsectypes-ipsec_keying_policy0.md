---
UID: NS:ipsectypes.IPSEC_KEYING_POLICY0_
title: IPSEC_KEYING_POLICY0 (ipsectypes.h)

description: Defines an unordered set of keying modules that will be tried for IPsec.
old-location: fwp\ipsec_keying_policy0_struct.htm
tech.root: fwp
ms.assetid: 6eddafbf-ac57-419f-b2a0-f50a4ab31baf

ms.date: 12/05/2018
ms.keywords: IPSEC_KEYING_POLICY0, IPSEC_KEYING_POLICY0 structure [Filtering], fwp.ipsec_keying_policy0_struct, ipsectypes/IPSEC_KEYING_POLICY0
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_KEYING_POLICY0"
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
 - IPSEC_KEYING_POLICY0
targetos: Windows
req.typenames: IPSEC_KEYING_POLICY0
req.redist: 
ms.custom: 19H1
---

# IPSEC_KEYING_POLICY0 structure


## -description


The [IPSEC_KEYING_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)a> is available.</div>
<div> </div>



## -struct-fields




### -field numKeyMods

Number of keying modules in the array.


### -field keyModKeys

Array of distinct keying modules.


## -remarks



<b>IPSEC_KEYING_POLICY0</b> is a specific implementation of IPSEC_KEYING_POLICY. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

