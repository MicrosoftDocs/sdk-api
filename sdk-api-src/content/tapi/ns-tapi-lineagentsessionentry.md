---
UID: NS:tapi.lineagentsession_tag
title: LINEAGENTSESSIONENTRY (tapi.h)
description: The LINEAGENTSESSIONENTRY structure describes an ACD agent session. The LINEAGENTSESSIONLIST structure can contain an array of LINEAGENTSESSIONENTRY structures.
helpviewer_keywords: ["*LPLINEAGENTSESSIONENTRY","LINEAGENTSESSIONENTRY","LINEAGENTSESSIONENTRY structure [TAPI 2.2]","LPLINEAGENTSESSIONENTRY","LPLINEAGENTSESSIONENTRY structure pointer [TAPI 2.2]","_tapi2_lineagentsessionentry_str","tapi/LINEAGENTSESSIONENTRY","tapi/LPLINEAGENTSESSIONENTRY","tapi2.lineagentsessionentry_str"]
old-location: tapi2\lineagentsessionentry_str.htm
tech.root: tapi3
ms.assetid: 406b003a-11a2-445d-a466-a8549e201199
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTSESSIONENTRY, LINEAGENTSESSIONENTRY, LINEAGENTSESSIONENTRY structure [TAPI 2.2], LPLINEAGENTSESSIONENTRY, LPLINEAGENTSESSIONENTRY structure pointer [TAPI 2.2], _tapi2_lineagentsessionentry_str, tapi/LINEAGENTSESSIONENTRY, tapi/LPLINEAGENTSESSIONENTRY, tapi2.lineagentsessionentry_str'
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: LINEAGENTSESSIONENTRY, *LPLINEAGENTSESSIONENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentsession_tag
 - tapi/lineagentsession_tag
 - LPLINEAGENTSESSIONENTRY
 - tapi/LPLINEAGENTSESSIONENTRY
 - LINEAGENTSESSIONENTRY
 - tapi/LINEAGENTSESSIONENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTSESSIONENTRY
---

# LINEAGENTSESSIONENTRY structure


## -description

The 
<b>LINEAGENTSESSIONENTRY</b> structure describes an ACD agent session. The 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist">LINEAGENTSESSIONLIST</a> structure can contain an array of 
<b>LINEAGENTSESSIONENTRY</b> structures.

## -struct-fields

### -field hAgentSession

Unique identifier for an agent session. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.

### -field hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.

### -field GroupID

Universally unique identifier for an ACD group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.

### -field dwWorkingAddressID

Address identifier on which the agent will receive calls for this session.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist">LINEAGENTSESSIONLIST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessionlist">lineGetAgentSessionList</a>