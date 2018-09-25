---
UID: NE:ntsecapi.LSA_FOREST_TRUST_COLLISION_RECORD_TYPE
title: LSA_FOREST_TRUST_COLLISION_RECORD_TYPE
author: windows-sdk-content
description: Defines the types of collision that can occur between Local Security Authority forest trust records.
old-location: security\lsa_forest_trust_collision_record_type.htm
tech.root: secauthn
ms.assetid: 67c89d75-2c2d-4980-a1c9-32e7f64a7b49
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CollisionOther, CollisionTdo, CollisionXref, LSA_FOREST_TRUST_COLLISION_RECORD_TYPE, LSA_FOREST_TRUST_COLLISION_RECORD_TYPE enumeration [Security], ntsecapi/CollisionOther, ntsecapi/CollisionTdo, ntsecapi/CollisionXref, ntsecapi/LSA_FOREST_TRUST_COLLISION_RECORD_TYPE, security.lsa_forest_trust_collision_record_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_COLLISION_RECORD_TYPE
product: Windows
targetos: Windows
req.typenames: LSA_FOREST_TRUST_COLLISION_RECORD_TYPE
req.redist: 
---

# LSA_FOREST_TRUST_COLLISION_RECORD_TYPE enumeration


## -description


The <b>LSA_FOREST_TRUST_COLLISION_RECORD_TYPE</b> enumeration defines the types of collision that can occur between <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust records.


## -enum-fields




### -field CollisionTdo

Collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects. This indicates a collision with a namespace element of another forest.


### -field CollisionXref

Collision between cross-references. This indicates a collision with a domain in the same forest.


### -field CollisionOther

Collision that is not a collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects or cross-references.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structure.



