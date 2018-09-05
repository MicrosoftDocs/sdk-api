---
UID: NE:ntsecapi.LSA_FOREST_TRUST_RECORD_TYPE
title: LSA_FOREST_TRUST_RECORD_TYPE
author: windows-sdk-content
description: Defines the type of a Local Security Authority forest trust record.
old-location: security\lsa_forest_trust_record_type.htm
old-project: SecAuthN
ms.assetid: 8a4a7080-fab0-4ab2-a0b4-e929cce21f0c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ForestTrustDomainInfo, ForestTrustRecordTypeLast, ForestTrustTopLevelName, ForestTrustTopLevelNameEx, LSA_FOREST_TRUST_RECORD_TYPE, LSA_FOREST_TRUST_RECORD_TYPE enumeration [Security], ntsecapi/ForestTrustDomainInfo, ntsecapi/ForestTrustRecordTypeLast, ntsecapi/ForestTrustTopLevelName, ntsecapi/ForestTrustTopLevelNameEx, ntsecapi/LSA_FOREST_TRUST_RECORD_TYPE, security.lsa_forest_trust_record_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: LSA_FOREST_TRUST_RECORD_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_RECORD_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# LSA_FOREST_TRUST_RECORD_TYPE enumeration


## -description


The <b>LSA_FOREST_TRUST_RECORD_TYPE</b> enumeration defines the type of a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust record.


## -enum-fields




### -field ForestTrustTopLevelName

Record contains an included top-level name.


### -field ForestTrustTopLevelNameEx

Record contains an excluded top-level name.


### -field ForestTrustDomainInfo

Record contains an <a href="https://msdn.microsoft.com/c0e06735-ca10-4bee-a45b-6db5b6666e31">LSA_FOREST_TRUST_DOMAIN_INFO</a> structure.


### -field ForestTrustRecordTypeLast

Marks the end of an enumeration.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/19b4ee56-664f-4f37-bfc9-129032ebeb22">LSA_FOREST_TRUST_RECORD</a> structure.



