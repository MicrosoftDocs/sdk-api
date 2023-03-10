---
UID: NS:ipsectypes.IPSEC_KEYMODULE_STATE0_
title: IPSEC_KEYMODULE_STATE0 (ipsectypes.h)
description: Stores Internet Protocol Security (IPsec) keying module specific information.
helpviewer_keywords: ["IPSEC_KEYMODULE_STATE0","IPSEC_KEYMODULE_STATE0 structure [Filtering]","fwp.ipsec_keymodule_state0_struct","ipsectypes/IPSEC_KEYMODULE_STATE0"]
old-location: fwp\ipsec_keymodule_state0_struct.htm
tech.root: fwp
ms.assetid: 5df02d3b-c61a-4c4b-a9ef-182c97a35f41
ms.date: 12/05/2018
ms.keywords: IPSEC_KEYMODULE_STATE0, IPSEC_KEYMODULE_STATE0 structure [Filtering], fwp.ipsec_keymodule_state0_struct, ipsectypes/IPSEC_KEYMODULE_STATE0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_KEYMODULE_STATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_KEYMODULE_STATE0_
 - ipsectypes/IPSEC_KEYMODULE_STATE0_
 - IPSEC_KEYMODULE_STATE0
 - ipsectypes/IPSEC_KEYMODULE_STATE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_KEYMODULE_STATE0
---

# IPSEC_KEYMODULE_STATE0 structure


## -description

The <b>IPSEC_KEYMODULE_STATE0</b> structure stores Internet Protocol Security (IPsec) keying module specific information.

## -struct-fields

### -field keyModuleKey

The identifier of the keying module.

### -field stateBlob

A byte blob containing opaque keying module specific information.

## -remarks

<b>IPSEC_KEYMODULE_STATE0</b> is a specific implementation of IPSEC_KEYMODULE_STATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>