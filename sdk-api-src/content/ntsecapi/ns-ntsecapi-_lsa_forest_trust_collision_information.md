---
UID: NS:ntsecapi._LSA_FOREST_TRUST_COLLISION_INFORMATION
title: "_LSA_FOREST_TRUST_COLLISION_INFORMATION"
author: windows-sdk-content
description: Contains information about Local Security Authority forest trust collisions.
old-location: security\lsa_forest_trust_collision_information.htm
old-project: SecAuthN
ms.assetid: a4a3b040-c074-4756-a30f-408d8bca87ba
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PLSA_FOREST_TRUST_COLLISION_INFORMATION, LSA_FOREST_TRUST_COLLISION_INFORMATION, LSA_FOREST_TRUST_COLLISION_INFORMATION structure [Security], PLSA_FOREST_TRUST_COLLISION_INFORMATION, PLSA_FOREST_TRUST_COLLISION_INFORMATION structure pointer [Security], _LSA_FOREST_TRUST_COLLISION_INFORMATION, ntsecapi/LSA_FOREST_TRUST_COLLISION_INFORMATION, ntsecapi/PLSA_FOREST_TRUST_COLLISION_INFORMATION, security.lsa_forest_trust_collision_information"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: LSA_FOREST_TRUST_COLLISION_INFORMATION, *PLSA_FOREST_TRUST_COLLISION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_COLLISION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _LSA_FOREST_TRUST_COLLISION_INFORMATION structure


## -description


The <b>LSA_FOREST_TRUST_COLLISION_INFORMATION</b> structure contains information about <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust collisions.


## -struct-fields




### -field RecordCount

Number of <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures in the array pointed to by the <b>Entries</b> member.


### -field Entries

Pointer to a pointer to an array of <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures, each of which contains information about a single collision.


### -field Entries.size_is

 


### -field Entries.size_is.RecordCount

 



