---
UID: NE:ndhelper.tagREPAIR_STATUS
title: REPAIR_STATUS (ndhelper.h)
description: The REPAIR_STATUS enumeration describes the result of a helper class attempting a repair option.
helpviewer_keywords: ["REPAIR_STATUS","REPAIR_STATUS enumeration [NDF]","RS_DEFERRED","RS_NOT_IMPLEMENTED","RS_REPAIRED","RS_UNREPAIRED","RS_USER_ACTION","ndf.repair_status","ndhelper/REPAIR_STATUS","ndhelper/RS_DEFERRED","ndhelper/RS_NOT_IMPLEMENTED","ndhelper/RS_REPAIRED","ndhelper/RS_UNREPAIRED","ndhelper/RS_USER_ACTION"]
old-location: ndf\repair_status.htm
tech.root: NDF
ms.assetid: efc3b64f-d3f3-41da-ae43-c7d8df9bf8e1
ms.date: 12/05/2018
ms.keywords: REPAIR_STATUS, REPAIR_STATUS enumeration [NDF], RS_DEFERRED, RS_NOT_IMPLEMENTED, RS_REPAIRED, RS_UNREPAIRED, RS_USER_ACTION, ndf.repair_status, ndhelper/REPAIR_STATUS, ndhelper/RS_DEFERRED, ndhelper/RS_NOT_IMPLEMENTED, ndhelper/RS_REPAIRED, ndhelper/RS_UNREPAIRED, ndhelper/RS_USER_ACTION
req.header: ndhelper.h
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
req.typenames: REPAIR_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREPAIR_STATUS
 - ndhelper/tagREPAIR_STATUS
 - REPAIR_STATUS
 - ndhelper/REPAIR_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - REPAIR_STATUS
---

# REPAIR_STATUS enumeration


## -description

The <b>REPAIR_STATUS</b> enumeration describes the result of a helper class attempting a repair option.

## -enum-fields

### -field RS_NOT_IMPLEMENTED:0

The helper class does not have a repair option implemented.

### -field RS_REPAIRED

The helper class has repaired a problem.

### -field RS_UNREPAIRED

The helper class has attempted to repair a problem but validation indicates the repair operation has not succeeded.

### -field RS_DEFERRED

The helper class is unable to perform the repair at this time.

### -field RS_USER_ACTION

The helper class needs the user to perform an action before the repair can continue.

