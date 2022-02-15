---
UID: NE:ndattrib.tagREPAIR_SCOPE
title: REPAIR_SCOPE (ndattrib.h)
description: The REPAIR_SCOPE enumeration describes the scope of modification for a given repair.
helpviewer_keywords: ["*PREPAIR_SCOPE","REPAIR_SCOPE","REPAIR_SCOPE enumeration [NDF]","RS_APPLICATION","RS_PROCESS","RS_SYSTEM","RS_USER","ndattrib/REPAIR_SCOPE","ndattrib/RS_APPLICATION","ndattrib/RS_PROCESS","ndattrib/RS_SYSTEM","ndattrib/RS_USER","ndf.repair_scope"]
old-location: ndf\repair_scope.htm
tech.root: NDF
ms.assetid: f9be87ae-82a1-4613-abeb-15ccba1bf360
ms.date: 12/05/2018
ms.keywords: '*PREPAIR_SCOPE, REPAIR_SCOPE, REPAIR_SCOPE enumeration [NDF], RS_APPLICATION, RS_PROCESS, RS_SYSTEM, RS_USER, ndattrib/REPAIR_SCOPE, ndattrib/RS_APPLICATION, ndattrib/RS_PROCESS, ndattrib/RS_SYSTEM, ndattrib/RS_USER, ndf.repair_scope'
req.header: ndattrib.h
req.include-header: 
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
req.typenames: REPAIR_SCOPE, *PREPAIR_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREPAIR_SCOPE
 - ndattrib/tagREPAIR_SCOPE
 - PREPAIR_SCOPE
 - ndattrib/PREPAIR_SCOPE
 - REPAIR_SCOPE
 - ndattrib/REPAIR_SCOPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ndattrib.h
api_name:
 - REPAIR_SCOPE
---

# REPAIR_SCOPE enumeration


## -description

The <b>REPAIR_SCOPE</b> enumeration describes the scope of modification for a given repair.

## -enum-fields

### -field RS_SYSTEM:0

The repair effect is system-wide.

### -field RS_USER

The repair effect is user-specific.

### -field RS_APPLICATION

The repair effect is application-specific.

### -field RS_PROCESS

The repair effect is process-specific.

