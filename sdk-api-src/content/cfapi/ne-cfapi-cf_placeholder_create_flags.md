---
UID: NE:cfapi.CF_PLACEHOLDER_CREATE_FLAGS
title: CF_PLACEHOLDER_CREATE_FLAGS (cfapi.h)
description: Flags for creating a placeholder on a per-placeholder basis.helpviewer_keywords: ["CF_PLACEHOLDER_CREATE_FLAGS","CF_PLACEHOLDER_CREATE_FLAGS enumeration","CF_PLACEHOLDER_CREATE_FLAG_DISABLE_ON_DEMAND_POPULATION","CF_PLACEHOLDER_CREATE_FLAG_MARK_IN_SYNC","CF_PLACEHOLDER_CREATE_FLAG_NONE","cfapi/CF_PLACEHOLDER_CREATE_FLAGS","cfapi/CF_PLACEHOLDER_CREATE_FLAG_DISABLE_ON_DEMAND_POPULATION","cfapi/CF_PLACEHOLDER_CREATE_FLAG_MARK_IN_SYNC","cfapi/CF_PLACEHOLDER_CREATE_FLAG_NONE","cloudApi.cf_placeholder_create_flags"]
old-location: cloudapi\cf_placeholder_create_flags.htm
tech.root: cfApi
ms.assetid: 7DB55949-E209-490C-9FF9-53E1D72CD0FA
ms.date: 12/05/2018
ms.keywords: CF_PLACEHOLDER_CREATE_FLAGS, CF_PLACEHOLDER_CREATE_FLAGS enumeration, CF_PLACEHOLDER_CREATE_FLAG_DISABLE_ON_DEMAND_POPULATION, CF_PLACEHOLDER_CREATE_FLAG_MARK_IN_SYNC, CF_PLACEHOLDER_CREATE_FLAG_NONE, cfapi/CF_PLACEHOLDER_CREATE_FLAGS, cfapi/CF_PLACEHOLDER_CREATE_FLAG_DISABLE_ON_DEMAND_POPULATION, cfapi/CF_PLACEHOLDER_CREATE_FLAG_MARK_IN_SYNC, cfapi/CF_PLACEHOLDER_CREATE_FLAG_NONE, cloudApi.cf_placeholder_create_flags
f1_keywords:
- cfapi/CF_PLACEHOLDER_CREATE_FLAGS
dev_langs:
- c++
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- CfApi.h
api_name:
- CF_PLACEHOLDER_CREATE_FLAGS
targetos: Windows
req.typenames: CF_PLACEHOLDER_CREATE_FLAGS
req.redist: 
ms.custom: 19H1
---

# CF_PLACEHOLDER_CREATE_FLAGS enumeration


## -description


Flags for creating a placeholder on a per-placeholder basis.


## -enum-fields




### -field CF_PLACEHOLDER_CREATE_FLAG_NONE

No placeholder create flags.


### -field CF_PLACEHOLDER_CREATE_FLAG_DISABLE_ON_DEMAND_POPULATION

The newly created child placeholder directory is considered to have all of its children present locally.

Applicable to a child placeholder directory only.


### -field CF_PLACEHOLDER_CREATE_FLAG_MARK_IN_SYNC

The newly created placeholder is marked as in-sync. Applicable to both placeholder files and directories.


### -field CF_PLACEHOLDER_CREATE_FLAG_SUPERSEDE



