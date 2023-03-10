---
UID: NE:ntsecapi.LSA_FOREST_TRUST_RECORD_TYPE
title: LSA_FOREST_TRUST_RECORD_TYPE (ntsecapi.h)
description: Defines the type of a Local Security Authority forest trust record.
helpviewer_keywords: ["ForestTrustDomainInfo","ForestTrustRecordTypeLast","ForestTrustTopLevelName","ForestTrustTopLevelNameEx","LSA_FOREST_TRUST_RECORD_TYPE","LSA_FOREST_TRUST_RECORD_TYPE enumeration [Security]","ntsecapi/ForestTrustDomainInfo","ntsecapi/ForestTrustRecordTypeLast","ntsecapi/ForestTrustTopLevelName","ntsecapi/ForestTrustTopLevelNameEx","ntsecapi/LSA_FOREST_TRUST_RECORD_TYPE","security.lsa_forest_trust_record_type"]
old-location: security\lsa_forest_trust_record_type.htm
tech.root: security
ms.assetid: 8a4a7080-fab0-4ab2-a0b4-e929cce21f0c
ms.date: 12/05/2018
ms.keywords: ForestTrustDomainInfo, ForestTrustRecordTypeLast, ForestTrustTopLevelName, ForestTrustTopLevelNameEx, LSA_FOREST_TRUST_RECORD_TYPE, LSA_FOREST_TRUST_RECORD_TYPE enumeration [Security], ntsecapi/ForestTrustDomainInfo, ntsecapi/ForestTrustRecordTypeLast, ntsecapi/ForestTrustTopLevelName, ntsecapi/ForestTrustTopLevelNameEx, ntsecapi/LSA_FOREST_TRUST_RECORD_TYPE, security.lsa_forest_trust_record_type
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
req.typenames: LSA_FOREST_TRUST_RECORD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_FOREST_TRUST_RECORD_TYPE
 - ntsecapi/LSA_FOREST_TRUST_RECORD_TYPE
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
 - LSA_FOREST_TRUST_RECORD_TYPE
---

# LSA_FOREST_TRUST_RECORD_TYPE enumeration


## -description

The <b>LSA_FOREST_TRUST_RECORD_TYPE</b> enumeration defines the type of a <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> forest trust record.

## -enum-fields

### -field ForestTrustTopLevelName

Record contains an included top-level name.

### -field ForestTrustTopLevelNameEx

Record contains an excluded top-level name.

### -field ForestTrustDomainInfo

Record contains an <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_domain_info">LSA_FOREST_TRUST_DOMAIN_INFO</a> structure.

### -field ForestTrustRecordTypeLast

Marks the end of an enumeration.

## -remarks

This enumeration is used by the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_record">LSA_FOREST_TRUST_RECORD</a> structure.

