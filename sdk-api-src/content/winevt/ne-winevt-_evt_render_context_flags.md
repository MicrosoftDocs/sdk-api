---
UID: NE:winevt._EVT_RENDER_CONTEXT_FLAGS
title: "_EVT_RENDER_CONTEXT_FLAGS"
author: windows-sdk-content
description: Defines the values that specify the type of information to access from the event.
old-location: wes\evt_render_context_flags.htm
old-project: wes
ms.assetid: 1c933266-28d9-4ef2-b156-eedf4ccb189b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EVT_RENDER_CONTEXT_FLAGS, EVT_RENDER_CONTEXT_FLAGS enumeration [EventLog], EvtRenderContextSystem, EvtRenderContextUser, EvtRenderContextValues, _EVT_RENDER_CONTEXT_FLAGS, wes.evt_render_context_flags, winevt/EVT_RENDER_CONTEXT_FLAGS, winevt/EvtRenderContextSystem, winevt/EvtRenderContextUser, winevt/EvtRenderContextValues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winevt.h
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
tech.root: 
req.typenames: EVT_RENDER_CONTEXT_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_RENDER_CONTEXT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _EVT_RENDER_CONTEXT_FLAGS enumeration


## -description


Defines the values that specify the type of information to access from the event.


## -enum-fields




### -field EvtRenderContextValues

Render specific properties from the event.


### -field EvtRenderContextSystem

Render the system properties under the <b>System</b> element. The properties are returned in the order defined in the <a href="https://msdn.microsoft.com/a77cfbac-9abd-41e1-8ce6-ba92de97eb64">EVT_SYSTEM_PROPERTY_ID</a> enumeration.


### -field EvtRenderContextUser

Render all user-defined properties under the <b>UserData</b> or <b>EventData</b> element. If the data template associated with the event contains a <b>UserData</b> section, the <b>UserData</b> properties are rendered; otherwise, the <b>EventData</b> properties are rendered.


## -remarks



You cannot specify the EvtRenderContextValues flag with the EvtRenderContextSystem or EvtRenderContextUser flag.




## -see-also




<a href="https://msdn.microsoft.com/729cfd74-c158-463d-9247-ee2c75b259d4">EvtCreateRenderContext</a>
 

 

