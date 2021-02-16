---
UID: NS:ntsecapi._LSA_FOREST_TRUST_COLLISION_INFORMATION
title: LSA_FOREST_TRUST_COLLISION_INFORMATION (ntsecapi.h)
description: Contains information about Local Security Authority forest trust collisions.
helpviewer_keywords: ["*PLSA_FOREST_TRUST_COLLISION_INFORMATION","LSA_FOREST_TRUST_COLLISION_INFORMATION","LSA_FOREST_TRUST_COLLISION_INFORMATION structure [Security]","PLSA_FOREST_TRUST_COLLISION_INFORMATION","PLSA_FOREST_TRUST_COLLISION_INFORMATION structure pointer [Security]","_LSA_FOREST_TRUST_COLLISION_INFORMATION","ntsecapi/LSA_FOREST_TRUST_COLLISION_INFORMATION","ntsecapi/PLSA_FOREST_TRUST_COLLISION_INFORMATION","security.lsa_forest_trust_collision_information"]
old-location: security\lsa_forest_trust_collision_information.htm
tech.root: security
ms.assetid: a4a3b040-c074-4756-a30f-408d8bca87ba
ms.date: 12/05/2018
ms.keywords: '*PLSA_FOREST_TRUST_COLLISION_INFORMATION, LSA_FOREST_TRUST_COLLISION_INFORMATION, LSA_FOREST_TRUST_COLLISION_INFORMATION structure [Security], PLSA_FOREST_TRUST_COLLISION_INFORMATION, PLSA_FOREST_TRUST_COLLISION_INFORMATION structure pointer [Security], _LSA_FOREST_TRUST_COLLISION_INFORMATION, ntsecapi/LSA_FOREST_TRUST_COLLISION_INFORMATION, ntsecapi/PLSA_FOREST_TRUST_COLLISION_INFORMATION, security.lsa_forest_trust_collision_information'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
targetos: Windows
req.typenames: LSA_FOREST_TRUST_COLLISION_INFORMATION, *PLSA_FOREST_TRUST_COLLISION_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_FOREST_TRUST_COLLISION_INFORMATION
 - ntsecapi/_LSA_FOREST_TRUST_COLLISION_INFORMATION
 - PLSA_FOREST_TRUST_COLLISION_INFORMATION
 - ntsecapi/PLSA_FOREST_TRUST_COLLISION_INFORMATION
 - LSA_FOREST_TRUST_COLLISION_INFORMATION
 - ntsecapi/LSA_FOREST_TRUST_COLLISION_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_COLLISION_INFORMATION
---

# LSA_FOREST_TRUST_COLLISION_INFORMATION structure


## -description

The <b>LSA_FOREST_TRUST_COLLISION_INFORMATION</b> structure contains information about <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> forest trust collisions.

## -struct-fields

### -field RecordCount

Number of <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_collision_record">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures in the array pointed to by the <b>Entries</b> member.

### -field Entries

Pointer to a pointer to an array of <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_collision_record">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures, each of which contains information about a single collision.

### -field Entries.size_is

### -field Entries.size_is.RecordCount