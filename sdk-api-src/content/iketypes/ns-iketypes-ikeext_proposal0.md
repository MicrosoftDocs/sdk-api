---
UID: NS:iketypes.IKEEXT_PROPOSAL0_
title: IKEEXT_PROPOSAL0 (iketypes.h)
description: Is used to store an IKE/AuthIP main mode proposal.
helpviewer_keywords: ["IKEEXT_PROPOSAL0","IKEEXT_PROPOSAL0 structure [Filtering]","fwp.ikeext_proposal0","iketypes/IKEEXT_PROPOSAL0"]
old-location: fwp\ikeext_proposal0.htm
tech.root: fwp
ms.assetid: 59568ef7-12bd-407a-a8ee-9bf261f49883
ms.date: 12/05/2018
ms.keywords: IKEEXT_PROPOSAL0, IKEEXT_PROPOSAL0 structure [Filtering], fwp.ikeext_proposal0, iketypes/IKEEXT_PROPOSAL0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_PROPOSAL0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_PROPOSAL0_
 - iketypes/IKEEXT_PROPOSAL0_
 - IKEEXT_PROPOSAL0
 - iketypes/IKEEXT_PROPOSAL0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_PROPOSAL0
---

# IKEEXT_PROPOSAL0 structure


## -description

The <b>IKEEXT_PROPOSAL0</b> structure is used to store an IKE/AuthIP main mode proposal.

## -struct-fields

### -field cipherAlgorithm

Parameters for the encryption algorithm specified by [IKEEXT_CIPHER_ALGORITHM0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cipher_algorithm0).

### -field integrityAlgorithm

Parameters for the hash algorithm specified by [IKEEXT_INTEGRITY_ALGORITHM0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_integrity_algorithm0).

### -field maxLifetimeSeconds

Main mode security association (SA) lifetime in seconds.

### -field dhGroup

The Diffie Hellman group specified by [IKEEXT_DH_GROUP](/windows/desktop/api/iketypes/ne-iketypes-ikeext_dh_group).

### -field quickModeLimit

Maximum number of IPsec quick mode SAs that can be generated from this
   main mode SA. 0 (zero) means infinite.

## -remarks

The proposal describes the
various parameters of the IKE/AuthIP main mode SA that is potentially generated
from this proposal.

<b>IKEEXT_PROPOSAL0</b> is a specific implementation of IKEEXT_PROPOSAL. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IKEEXT_CIPHER_ALGORITHM0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cipher_algorithm0)



[IKEEXT_DH_GROUP](/windows/desktop/api/iketypes/ne-iketypes-ikeext_dh_group)



[IKEEXT_INTEGRITY_ALGORITHM0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_integrity_algorithm0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>