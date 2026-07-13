---
UID: NS:lpmapi.RSVP_SCOPE
title: RSVP_SCOPE (lpmapi.h)
description: The RSVP_SCOPE structure provides RSVP scope information.
helpviewer_keywords: ["RSVP_SCOPE","RSVP_SCOPE structure [QOS]","lpmapi/RSVP_SCOPE","qos.rsvp_scope"]
old-location: qos\rsvp_scope.htm
tech.root: QOS
ms.assetid: 64a7e461-d767-4571-97ca-cf7862a05d18
ms.date: 12/05/2018
ms.keywords: RSVP_SCOPE, RSVP_SCOPE structure [QOS], lpmapi/RSVP_SCOPE, qos.rsvp_scope
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RSVP_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RSVP_SCOPE
 - lpmapi/RSVP_SCOPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - RSVP_SCOPE
---

# RSVP_SCOPE structure


## -description

The 
<b>RSVP_SCOPE</b> structure provides RSVP scope information.

## -struct-fields

### -field scopl_header

Scope header, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field scope_u

Union containing scope list information.



#### scopl_ipv4

RSVP scope list, in the form of a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-scope_list_ipv4">Scope_list_ipv4</a> structure.

### -field scopl_ipv4

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-scope_list_ipv4">Scope_list_ipv4</a>

