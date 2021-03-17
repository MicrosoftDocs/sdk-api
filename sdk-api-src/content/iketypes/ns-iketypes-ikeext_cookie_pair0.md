---
UID: NS:iketypes.IKEEXT_COOKIE_PAIR0_
title: IKEEXT_COOKIE_PAIR0 (iketypes.h)
description: Used to store a pair of IKE/Authip cookies.
helpviewer_keywords: ["IKEEXT_COOKIE_PAIR0","IKEEXT_COOKIE_PAIR0 structure [Filtering]","fwp.ikeext_cookie_pair0","iketypes/IKEEXT_COOKIE_PAIR0"]
old-location: fwp\ikeext_cookie_pair0.htm
tech.root: fwp
ms.assetid: c752545b-1880-40ac-871e-e36d4b81668f
ms.date: 12/05/2018
ms.keywords: IKEEXT_COOKIE_PAIR0, IKEEXT_COOKIE_PAIR0 structure [Filtering], fwp.ikeext_cookie_pair0, iketypes/IKEEXT_COOKIE_PAIR0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_COOKIE_PAIR0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_COOKIE_PAIR0_
 - iketypes/IKEEXT_COOKIE_PAIR0_
 - IKEEXT_COOKIE_PAIR0
 - iketypes/IKEEXT_COOKIE_PAIR0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_COOKIE_PAIR0
---

# IKEEXT_COOKIE_PAIR0 structure


## -description

The <b>IKEEXT_COOKIE_PAIR0</b> structure used to store a pair of IKE/Authip cookies.

## -struct-fields

### -field initiator

Initiator cookie. An IKEEXT_COOKIE is a UINT64.

### -field responder

Responder cookie. An IKEEXT_COOKIE is a UINT64.

## -remarks

<b>IKEEXT_COOKIE_PAIR0</b> is a specific implementation of IKEEXT_COOKIE_PAIR. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>