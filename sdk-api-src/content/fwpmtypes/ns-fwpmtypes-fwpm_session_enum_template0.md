---
UID: NS:fwpmtypes.FWPM_SESSION_ENUM_TEMPLATE0_
title: FWPM_SESSION_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Used for enumerating sessions.
helpviewer_keywords: ["FWPM_SESSION_ENUM_TEMPLATE0","FWPM_SESSION_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_session_enum_template0_struct","fwpmtypes/FWPM_SESSION_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_session_enum_template0_struct.htm
tech.root: fwp
ms.assetid: d95fff0c-2f80-4ae4-9d75-9c7b0220a902
ms.date: 12/05/2018
ms.keywords: FWPM_SESSION_ENUM_TEMPLATE0, FWPM_SESSION_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_session_enum_template0_struct, fwpmtypes/FWPM_SESSION_ENUM_TEMPLATE0
req.header: fwpmtypes.h
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
req.typenames: FWPM_SESSION_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SESSION_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_SESSION_ENUM_TEMPLATE0_
 - FWPM_SESSION_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_SESSION_ENUM_TEMPLATE0
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
 - FWPM_SESSION_ENUM_TEMPLATE0
---

# FWPM_SESSION_ENUM_TEMPLATE0 structure


## -description

The <b>FWPM_SESSION_ENUM_TEMPLATE0</b> structure is used for enumerating sessions.

## -struct-fields

### -field reserved

Reserved for system use.

## -remarks

Currently, there is no way to limit the
enumeration — all sessions are returned.

<b>FWPM_SESSION_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_SESSION_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0">FwpmSessionCreateEnumHandle0</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>