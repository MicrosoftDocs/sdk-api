---
UID: NS:ntsecapi._LSA_FOREST_TRUST_INFORMATION
title: LSA_FOREST_TRUST_INFORMATION (ntsecapi.h)
description: Contains Local Security Authority forest trust information.
helpviewer_keywords: ["*PLSA_FOREST_TRUST_INFORMATION","LSA_FOREST_TRUST_INFORMATION","LSA_FOREST_TRUST_INFORMATION structure [Security]","PLSA_FOREST_TRUST_INFORMATION","PLSA_FOREST_TRUST_INFORMATION structure pointer [Security]","_LSA_FOREST_TRUST_INFORMATION","ntsecapi/LSA_FOREST_TRUST_INFORMATION","ntsecapi/PLSA_FOREST_TRUST_INFORMATION","security.lsa_forest_trust_information"]
old-location: security\lsa_forest_trust_information.htm
tech.root: security
ms.assetid: 9e456462-59a9-4f18-ba47-92fc2350889b
ms.date: 12/05/2018
ms.keywords: '*PLSA_FOREST_TRUST_INFORMATION, LSA_FOREST_TRUST_INFORMATION, LSA_FOREST_TRUST_INFORMATION structure [Security], PLSA_FOREST_TRUST_INFORMATION, PLSA_FOREST_TRUST_INFORMATION structure pointer [Security], _LSA_FOREST_TRUST_INFORMATION, ntsecapi/LSA_FOREST_TRUST_INFORMATION, ntsecapi/PLSA_FOREST_TRUST_INFORMATION, security.lsa_forest_trust_information'
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
req.typenames: LSA_FOREST_TRUST_INFORMATION, *PLSA_FOREST_TRUST_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_FOREST_TRUST_INFORMATION
 - ntsecapi/_LSA_FOREST_TRUST_INFORMATION
 - PLSA_FOREST_TRUST_INFORMATION
 - ntsecapi/PLSA_FOREST_TRUST_INFORMATION
 - LSA_FOREST_TRUST_INFORMATION
 - ntsecapi/LSA_FOREST_TRUST_INFORMATION
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
 - LSA_FOREST_TRUST_INFORMATION
---

# LSA_FOREST_TRUST_INFORMATION structure


## -description

The <b>LSA_FOREST_TRUST_INFORMATION</b> structure contains <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> forest trust information.

## -struct-fields

### -field RecordCount.range

### -field RecordCount.range.0

### -field RecordCount.range.MAX_RECORDS_IN_FOREST_TRUST_INFO

### -field Entries.size_is

### -field Entries.size_is.RecordCount

### -field RecordCount

Number of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_record">LSA_FOREST_TRUST_RECORD</a> structures in the array pointed to by the <b>Entries</b> member.

### -field Entries

Pointer to a pointer to an array of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_record">LSA_FOREST_TRUST_RECORD</a> structures, each of which contains one piece of forest trust information.