---
UID: NE:sessdirpublictypes._TARGET_TYPE
title: "_TARGET_TYPE"
author: windows-sdk-content
description: Indicates whether a target belongs to a pool or farm.
old-location: termserv\target_type.htm
old-project: termserv
ms.assetid: 4ad44a75-0975-4933-a914-a64a82fcae6c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FARM, NONFARM, TARGET_TYPE, TARGET_TYPE enumeration [Remote Desktop Services], UNKNOWN, _TARGET_TYPE, sessdirpublictypes/FARM, sessdirpublictypes/NONFARM, sessdirpublictypes/TARGET_TYPE, sessdirpublictypes/UNKNOWN, termserv.target_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: TARGET_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - TARGET_TYPE
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# _TARGET_TYPE enumeration


## -description


Indicates whether a target belongs to a pool or farm.


## -enum-fields




### -field UNKNOWN

The target type is unknown.


### -field FARM

The target is a virtual machine that belongs to a pool or an RD Session Host server that belongs to a farm.


### -field NONFARM

The target does not belong to a pool or farm.

