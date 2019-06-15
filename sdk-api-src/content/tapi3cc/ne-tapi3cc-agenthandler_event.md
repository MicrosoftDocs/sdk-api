---
UID: NE:tapi3cc.AGENTHANDLER_EVENT
title: AGENTHANDLER_EVENT (tapi3cc.h)
author: windows-sdk-content
description: The AGENTHANDLER_EVENT enum describes agent handler events. The ITAgentHandlerEvent::get_Event method returns a member of this enum to indicate the type of agent handler event that occurred.
old-location: tapi3\agenthandler_event.htm
tech.root: Tapi
ms.assetid: 6d8340a9-dfe5-43bc-a223-d534f5b90cba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AGENTHANDLER_EVENT, AGENTHANDLER_EVENT enumeration [TAPI 2.2], AHE_AGENTHANDLER_REMOVED, AHE_NEW_AGENTHANDLER, _tapi3_agenthandler_event, tapi3.agenthandler_event, tapi3cc/AGENTHANDLER_EVENT, tapi3cc/AHE_AGENTHANDLER_REMOVED, tapi3cc/AHE_NEW_AGENTHANDLER
ms.topic: enum
req.header: tapi3cc.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - AGENTHANDLER_EVENT
product: Windows
targetos: Windows
req.typenames: AGENTHANDLER_EVENT
req.redist: 
ms.custom: 19H1
---

# AGENTHANDLER_EVENT enumeration


## -description


The 
<b>AGENTHANDLER_EVENT</b> enum describes agent handler events. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_event">ITAgentHandlerEvent::get_Event</a> method returns a member of this enum to indicate the type of agent handler event that occurred.


## -enum-fields




### -field AHE_NEW_AGENTHANDLER

A new AgentHandler object has been added.


### -field AHE_AGENTHANDLER_REMOVED

An AgentHandler object has been removed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_event">ITAgentHandlerEvent::get_Event</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>
 

 

