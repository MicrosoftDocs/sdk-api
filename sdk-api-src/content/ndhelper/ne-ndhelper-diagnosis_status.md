---
UID: NE:ndhelper.tagDIAGNOSIS_STATUS
title: DIAGNOSIS_STATUS (ndhelper.h)
description: The DIAGNOSIS_STATUS enumeration describes the result of a hypothesis submitted to a helper class in which the health of a component has been determined.
helpviewer_keywords: ["DIAGNOSIS_STATUS","DIAGNOSIS_STATUS enumeration [NDF]","DS_CONFIRMED","DS_DEFERRED","DS_INDETERMINATE","DS_NOT_IMPLEMENTED","DS_PASSTHROUGH","DS_REJECTED","ndf.diagnosis_status","ndhelper/DIAGNOSIS_STATUS","ndhelper/DS_CONFIRMED","ndhelper/DS_DEFERRED","ndhelper/DS_INDETERMINATE","ndhelper/DS_NOT_IMPLEMENTED","ndhelper/DS_PASSTHROUGH","ndhelper/DS_REJECTED"]
old-location: ndf\diagnosis_status.htm
tech.root: NDF
ms.assetid: 2ad72ac5-3f33-4206-be39-1cfe11ee840d
ms.date: 12/05/2018
ms.keywords: DIAGNOSIS_STATUS, DIAGNOSIS_STATUS enumeration [NDF], DS_CONFIRMED, DS_DEFERRED, DS_INDETERMINATE, DS_NOT_IMPLEMENTED, DS_PASSTHROUGH, DS_REJECTED, ndf.diagnosis_status, ndhelper/DIAGNOSIS_STATUS, ndhelper/DS_CONFIRMED, ndhelper/DS_DEFERRED, ndhelper/DS_INDETERMINATE, ndhelper/DS_NOT_IMPLEMENTED, ndhelper/DS_PASSTHROUGH, ndhelper/DS_REJECTED
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
req.typenames: DIAGNOSIS_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDIAGNOSIS_STATUS
 - ndhelper/tagDIAGNOSIS_STATUS
 - DIAGNOSIS_STATUS
 - ndhelper/DIAGNOSIS_STATUS
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
 - DIAGNOSIS_STATUS
---

# DIAGNOSIS_STATUS enumeration


## -description

The <b>DIAGNOSIS_STATUS</b> enumeration describes the result of a hypothesis submitted to a helper class in which the health of a component has been determined.

## -enum-fields

### -field DS_NOT_IMPLEMENTED:0

A helper class is not implemented

### -field DS_CONFIRMED

The helper class has confirmed a problem existing in its component.

### -field DS_REJECTED

The helper class has determined that no problem exists.

### -field DS_INDETERMINATE

The helper class is unable to determine whether there is a problem.

### -field DS_DEFERRED

The helper class is unable to perform the diagnosis at this time.

### -field DS_PASSTHROUGH

The helper class has identified hypotheses to investigate further, but did not identify any problems in its own component.

Equivalent to <b>DS_INDETERMINATE</b>, but is later updated to <b>DS_REJECTED</b> if no hypothesis is confirmed.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>

