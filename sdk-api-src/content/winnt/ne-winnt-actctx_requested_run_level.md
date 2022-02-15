---
UID: NE:winnt.__unnamed_enum_8
title: ACTCTX_REQUESTED_RUN_LEVEL (winnt.h)
description: The ACTCTX_REQUESTED_RUN_LEVEL enumeration describes the requested run level of the activation context.
helpviewer_keywords: ["ACTCTX_REQUESTED_RUN_LEVEL","ACTCTX_REQUESTED_RUN_LEVEL enumeration [Side-by-side Assemblies]","ACTCTX_RUN_LEVEL_AS_INVOKER","ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE","ACTCTX_RUN_LEVEL_NUMBERS","ACTCTX_RUN_LEVEL_REQUIRE_ADMIN","ACTCTX_RUN_LEVEL_UNSPECIFIED","setup.actctx_requested_run_level","winnt/ACTCTX_REQUESTED_RUN_LEVEL","winnt/ACTCTX_RUN_LEVEL_AS_INVOKER","winnt/ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE","winnt/ACTCTX_RUN_LEVEL_NUMBERS","winnt/ACTCTX_RUN_LEVEL_REQUIRE_ADMIN","winnt/ACTCTX_RUN_LEVEL_UNSPECIFIED"]
old-location: setup\actctx_requested_run_level.htm
tech.root: setup
ms.assetid: 3bf75a4d-a209-43e4-9fe2-f7da1602fc6c
ms.date: 12/05/2018
ms.keywords: ACTCTX_REQUESTED_RUN_LEVEL, ACTCTX_REQUESTED_RUN_LEVEL enumeration [Side-by-side Assemblies], ACTCTX_RUN_LEVEL_AS_INVOKER, ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE, ACTCTX_RUN_LEVEL_NUMBERS, ACTCTX_RUN_LEVEL_REQUIRE_ADMIN, ACTCTX_RUN_LEVEL_UNSPECIFIED, setup.actctx_requested_run_level, winnt/ACTCTX_REQUESTED_RUN_LEVEL, winnt/ACTCTX_RUN_LEVEL_AS_INVOKER, winnt/ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE, winnt/ACTCTX_RUN_LEVEL_NUMBERS, winnt/ACTCTX_RUN_LEVEL_REQUIRE_ADMIN, winnt/ACTCTX_RUN_LEVEL_UNSPECIFIED
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ACTCTX_REQUESTED_RUN_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ACTCTX_REQUESTED_RUN_LEVEL
 - winnt/ACTCTX_REQUESTED_RUN_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACTCTX_REQUESTED_RUN_LEVEL
---

# ACTCTX_REQUESTED_RUN_LEVEL enumeration


## -description

The <b>ACTCTX_REQUESTED_RUN_LEVEL</b> enumeration describes the requested run level of the activation context.

## -enum-fields

### -field ACTCTX_RUN_LEVEL_UNSPECIFIED:0

The application manifest does not specify a requested run level for the application.

### -field ACTCTX_RUN_LEVEL_AS_INVOKER

The application manifest requests the least privilege level to run the application.

### -field ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE

The application manifest requests the highest privilege level to run the application.

### -field ACTCTX_RUN_LEVEL_REQUIRE_ADMIN

The application manifest requests the administrator privilege level to run the application.

### -field ACTCTX_RUN_LEVEL_NUMBERS

Total number of possible run levels.

