---
UID: NE:fwpmtypes.FWPM_SERVICE_STATE_
title: FWPM_SERVICE_STATE (fwpmtypes.h)
description: Specifies the current state of the filter engine.
helpviewer_keywords: ["FWPM_SERVICE_RUNNING","FWPM_SERVICE_START_PENDING","FWPM_SERVICE_STATE","FWPM_SERVICE_STATE enumeration [Filtering]","FWPM_SERVICE_STATE_MAX","FWPM_SERVICE_STOPPED","FWPM_SERVICE_STOP_PENDING","fwp.fwpm_service_state","fwpmtypes/FWPM_SERVICE_RUNNING","fwpmtypes/FWPM_SERVICE_START_PENDING","fwpmtypes/FWPM_SERVICE_STATE","fwpmtypes/FWPM_SERVICE_STATE_MAX","fwpmtypes/FWPM_SERVICE_STOPPED","fwpmtypes/FWPM_SERVICE_STOP_PENDING"]
old-location: fwp\fwpm_service_state.htm
tech.root: fwp
ms.assetid: 80a3695a-71ac-4c8b-897e-80c4231ad570
ms.date: 12/05/2018
ms.keywords: FWPM_SERVICE_RUNNING, FWPM_SERVICE_START_PENDING, FWPM_SERVICE_STATE, FWPM_SERVICE_STATE enumeration [Filtering], FWPM_SERVICE_STATE_MAX, FWPM_SERVICE_STOPPED, FWPM_SERVICE_STOP_PENDING, fwp.fwpm_service_state, fwpmtypes/FWPM_SERVICE_RUNNING, fwpmtypes/FWPM_SERVICE_START_PENDING, fwpmtypes/FWPM_SERVICE_STATE, fwpmtypes/FWPM_SERVICE_STATE_MAX, fwpmtypes/FWPM_SERVICE_STOPPED, fwpmtypes/FWPM_SERVICE_STOP_PENDING
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_SERVICE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SERVICE_STATE_
 - fwpmtypes/FWPM_SERVICE_STATE_
 - FWPM_SERVICE_STATE
 - fwpmtypes/FWPM_SERVICE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SERVICE_STATE
---

# FWPM_SERVICE_STATE enumeration


## -description

The <b>FWPM_SERVICE_STATE</b> enumeration specifies the current state of the filter engine.

## -enum-fields

### -field FWPM_SERVICE_STOPPED:0

The filter engine is not running.

### -field FWPM_SERVICE_START_PENDING

The filter engine is starting.

### -field FWPM_SERVICE_STOP_PENDING

The filter engine is stopping.

### -field FWPM_SERVICE_RUNNING

The filter engine is running.

### -field FWPM_SERVICE_STATE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
