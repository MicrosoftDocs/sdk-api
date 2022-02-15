---
UID: NE:tapi3.AGENTHANDLER_EVENT
title: AGENTHANDLER_EVENT (tapi3.h)
description: The AGENTHANDLER_EVENT enum describes agent handler events. The ITAgentHandlerEvent::get_Event method returns a member of this enum to indicate the type of agent handler event that occurred.
helpviewer_keywords: ["AGENTHANDLER_EVENT","AGENTHANDLER_EVENT enumeration [TAPI 2.2]","AHE_AGENTHANDLER_REMOVED","AHE_NEW_AGENTHANDLER","_tapi3_agenthandler_event","tapi3.agenthandler_event","tapi3cc/AGENTHANDLER_EVENT","tapi3cc/AHE_AGENTHANDLER_REMOVED","tapi3cc/AHE_NEW_AGENTHANDLER"]
old-location: tapi3\agenthandler_event.htm
tech.root: tapi3
ms.assetid: 6d8340a9-dfe5-43bc-a223-d534f5b90cba
ms.date: 12/05/2018
ms.keywords: AGENTHANDLER_EVENT, AGENTHANDLER_EVENT enumeration [TAPI 2.2], AHE_AGENTHANDLER_REMOVED, AHE_NEW_AGENTHANDLER, _tapi3_agenthandler_event, tapi3.agenthandler_event, tapi3cc/AGENTHANDLER_EVENT, tapi3cc/AHE_AGENTHANDLER_REMOVED, tapi3cc/AHE_NEW_AGENTHANDLER
req.header: tapi3.h
req.include-header: Tapi3.h
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
req.typenames: AGENTHANDLER_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AGENTHANDLER_EVENT
 - tapi3/AGENTHANDLER_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - AGENTHANDLER_EVENT
---

# AGENTHANDLER_EVENT enumeration


## -description

The 
<b>AGENTHANDLER_EVENT</b> enum describes agent handler events. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_event">ITAgentHandlerEvent::get_Event</a> method returns a member of this enum to indicate the type of agent handler event that occurred.

## -enum-fields

### -field AHE_NEW_AGENTHANDLER:0

A new AgentHandler object has been added.

### -field AHE_AGENTHANDLER_REMOVED

An AgentHandler object has been removed.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_event">ITAgentHandlerEvent::get_Event</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>
