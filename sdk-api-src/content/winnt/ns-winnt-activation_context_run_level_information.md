---
UID: NS:winnt._ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
title: ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION (winnt.h)
description: The ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure is used by the QueryActCtxW function.
helpviewer_keywords: ["*PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION","ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION","ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure [Side-by-side Assemblies]","PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION","PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure pointer [Side-by-side Assemblies]","_ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION","setup.activation_context_run_level_information","winnt/ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION","winnt/PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION"]
old-location: setup\activation_context_run_level_information.htm
tech.root: setup
ms.assetid: 1c4e7333-6982-4d58-ab2a-d1993c59d0ef
ms.date: 12/05/2018
ms.keywords: '*PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, setup.activation_context_run_level_information, winnt/ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, winnt/PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION'
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
req.typenames: ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION, *PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
 - winnt/_ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
 - PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
 - winnt/PACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
 - ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
 - winnt/ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
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
 - ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION
---

# ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure


## -description

The <b>ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION</b> structure is used by the <a href="/windows/desktop/api/winbase/nf-winbase-queryactctxw">QueryActCtxW</a> function.

## -struct-fields

### -field ulFlags

This parameter is reserved for future use. This parameter currently returns 0.

### -field RunLevel

A  <a href="/windows/desktop/api/winnt/ne-winnt-actctx_requested_run_level">ACTCTX_REQUESTED_RUN_LEVEL</a> enumeration value that gives the requested run level of the activation context.

### -field UiAccess

This parameter returns zero if the <b>uiAccess</b> attribute in the application manifest is false. This parameter returns a non-zero value if the <b>uiAccess</b> attribute in the manifest is true. True means that UI accessibility applications require access higher privileges.