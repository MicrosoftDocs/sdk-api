---
UID: NE:sessdirpublictypes._TARGET_TYPE
title: TARGET_TYPE (sessdirpublictypes.h)
description: Indicates whether a target belongs to a pool or farm.
helpviewer_keywords: ["FARM","NONFARM","TARGET_TYPE","TARGET_TYPE enumeration [Remote Desktop Services]","UNKNOWN","sessdirpublictypes/FARM","sessdirpublictypes/NONFARM","sessdirpublictypes/TARGET_TYPE","sessdirpublictypes/UNKNOWN","termserv.target_type"]
old-location: termserv\target_type.htm
tech.root: TermServ
ms.assetid: 4ad44a75-0975-4933-a914-a64a82fcae6c
ms.date: 12/05/2018
ms.keywords: FARM, NONFARM, TARGET_TYPE, TARGET_TYPE enumeration [Remote Desktop Services], UNKNOWN, sessdirpublictypes/FARM, sessdirpublictypes/NONFARM, sessdirpublictypes/TARGET_TYPE, sessdirpublictypes/UNKNOWN, termserv.target_type
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TARGET_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TARGET_TYPE
 - sessdirpublictypes/_TARGET_TYPE
 - TARGET_TYPE
 - sessdirpublictypes/TARGET_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - TARGET_TYPE
---

# TARGET_TYPE enumeration


## -description

Indicates whether a target belongs to a pool or farm.

## -enum-fields

### -field UNKNOWN:0

The target type is unknown.

### -field FARM:2

The target is a virtual machine that belongs to a pool or an RD Session Host server that belongs to a farm.

### -field NONFARM:2

The target does not belong to a pool or farm.

