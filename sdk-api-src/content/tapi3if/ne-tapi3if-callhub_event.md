---
UID: NE:tapi3if.CALLHUB_EVENT
title: CALLHUB_EVENT (tapi3if.h)
description: The CALLHUB_EVENT enum describes CallHub events. The ITCallHubEvent::get_Event method returns a member of this enum to indicate the type of CallHub event that occurred.
helpviewer_keywords: ["CALLHUB_EVENT","CALLHUB_EVENT enumeration [TAPI 2.2]","CHE_CALLHUBIDLE","CHE_CALLHUBNEW","CHE_CALLJOIN","CHE_CALLLEAVE","_tapi3_callhub_event","tapi3.callhub_event","tapi3if/CALLHUB_EVENT","tapi3if/CHE_CALLHUBIDLE","tapi3if/CHE_CALLHUBNEW","tapi3if/CHE_CALLJOIN","tapi3if/CHE_CALLLEAVE"]
old-location: tapi3\callhub_event.htm
tech.root: tapi3
ms.assetid: 199e6c8b-805c-40c6-80d0-2e5803ec85a1
ms.date: 12/05/2018
ms.keywords: CALLHUB_EVENT, CALLHUB_EVENT enumeration [TAPI 2.2], CHE_CALLHUBIDLE, CHE_CALLHUBNEW, CHE_CALLJOIN, CHE_CALLLEAVE, _tapi3_callhub_event, tapi3.callhub_event, tapi3if/CALLHUB_EVENT, tapi3if/CHE_CALLHUBIDLE, tapi3if/CHE_CALLHUBNEW, tapi3if/CHE_CALLJOIN, tapi3if/CHE_CALLLEAVE
req.header: tapi3if.h
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
req.typenames: CALLHUB_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLHUB_EVENT
 - tapi3if/CALLHUB_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALLHUB_EVENT
---

# CALLHUB_EVENT enumeration


## -description

The 
<b>CALLHUB_EVENT</b> enum describes CallHub events. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhubevent-get_event">ITCallHubEvent::get_Event</a> method returns a member of this enum to indicate the type of CallHub event that occurred.

## -enum-fields

### -field CHE_CALLJOIN:0

A new call has joined the CallHub.

### -field CHE_CALLLEAVE

A call has left the CallHub.

### -field CHE_CALLHUBNEW

A new CallHub has appeared.

### -field CHE_CALLHUBIDLE

A CallHub has gone idle.

### -field CHE_LASTITEM

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhubevent-get_event">ITCallHubEvent::get_Event</a>
