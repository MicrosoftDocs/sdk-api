---
UID: NE:tapi3if.CALLHUB_EVENT
title: CALLHUB_EVENT
author: windows-driver-content
description: The CALLHUB_EVENT enum describes CallHub events. The ITCallHubEvent::get_Event method returns a member of this enum to indicate the type of CallHub event that occurred.
old-location: tapi3\callhub_event.htm
old-project: Tapi
ms.assetid: 199e6c8b-805c-40c6-80d0-2e5803ec85a1
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CALLHUB_EVENT, CALLHUB_EVENT enumeration [TAPI 2.2], CHE_CALLHUBIDLE, CHE_CALLHUBNEW, CHE_CALLJOIN, CHE_CALLLEAVE, _tapi3_callhub_event, tapi3.callhub_event, tapi3if/CALLHUB_EVENT, tapi3if/CHE_CALLHUBIDLE, tapi3if/CHE_CALLHUBNEW, tapi3if/CHE_CALLJOIN, tapi3if/CHE_CALLLEAVE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: CALLHUB_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	CALLHUB_EVENT
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CALLHUB_EVENT enumeration


## -description


The 
<b>CALLHUB_EVENT</b> enum describes CallHub events. The 
<a href="https://msdn.microsoft.com/a2515583-e564-413d-b93f-6f2dd7776d7b">ITCallHubEvent::get_Event</a> method returns a member of this enum to indicate the type of CallHub event that occurred.


## -enum-fields




### -field CHE_CALLJOIN

A new call has joined the CallHub.


### -field CHE_CALLLEAVE

A call has left the CallHub.


### -field CHE_CALLHUBNEW

A new CallHub has appeared.


### -field CHE_CALLHUBIDLE

A CallHub has gone idle.


### -field CHE_LASTITEM




## -see-also




<a href="https://msdn.microsoft.com/a2515583-e564-413d-b93f-6f2dd7776d7b">ITCallHubEvent::get_Event</a>
 

 

