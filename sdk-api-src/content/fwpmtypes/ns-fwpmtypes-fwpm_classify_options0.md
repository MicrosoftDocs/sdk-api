---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTIONS0_
title: FWPM_CLASSIFY_OPTIONS0 (fwpmtypes.h)
description: The FWPM_CLASSIFY_OPTIONS0 structure is used to store FWPM_CLASSIFY_OPTION0 structures.
helpviewer_keywords: ["FWPM_CLASSIFY_OPTIONS0","FWPM_CLASSIFY_OPTIONS0 structure [Filtering]","FWPM_CLASSIFY_OPTIONS0_","fwp.fwpm_classify_options0","fwpmtypes/FWPM_CLASSIFY_OPTIONS0"]
old-location: fwp\fwpm_classify_options0.htm
tech.root: fwp
ms.assetid: 5d1f7807-4188-4a57-83fc-99683254e3a5
ms.date: 12/05/2018
ms.keywords: FWPM_CLASSIFY_OPTIONS0, FWPM_CLASSIFY_OPTIONS0 structure [Filtering], FWPM_CLASSIFY_OPTIONS0_, fwp.fwpm_classify_options0, fwpmtypes/FWPM_CLASSIFY_OPTIONS0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_CLASSIFY_OPTIONS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_CLASSIFY_OPTIONS0_
 - fwpmtypes/FWPM_CLASSIFY_OPTIONS0_
 - FWPM_CLASSIFY_OPTIONS0
 - fwpmtypes/FWPM_CLASSIFY_OPTIONS0
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
 - FWPM_CLASSIFY_OPTIONS0
---

# FWPM_CLASSIFY_OPTIONS0 structure


## -description

 The <b>FWPM_CLASSIFY_OPTIONS0</b> structure is used to store <b>FWPM_CLASSIFY_OPTION0</b> structures.

## -struct-fields

### -field numOptions

Number of <b>FWPM_CLASSIFY_OPTION0</b> structures in the <b>options</b> member.

### -field options

[size_is(numCredentials)]

Pointer to an array of [FWPM_CLASSIFY_OPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) structures.

## -remarks

<b>FWPM_CLASSIFY_OPTIONS0</b> is a specific implementation of FWPM_CLASSIFY_OPTIONS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CLASSIFY_OPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>