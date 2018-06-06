---
UID: NF:ocidl.IOleControl.FreezeEvents
title: IOleControl::FreezeEvents
author: windows-sdk-content
description: Indicates whether the container is ignoring or accepting events from the control.
old-location: com\iolecontrol_freezeevents.htm
old-project: com
ms.assetid: 08872f4f-eb3e-434c-bd7d-d4de621948ad
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: FreezeEvents, FreezeEvents method [COM], FreezeEvents method [COM],IOleControl interface, IOleControl interface [COM],FreezeEvents method, IOleControl.FreezeEvents, IOleControl::FreezeEvents, _ctrl_iolecontrol_freezeevents, com.iolecontrol_freezeevents, ocidl/IOleControl::FreezeEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControl.FreezeEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleControl::FreezeEvents


## -description


Indicates whether the container is ignoring or accepting events from the control.


## -parameters




### -param bFreeze [in]

Indicates whether the container will ignore (<b>TRUE</b>) or now process (<b>FALSE</b>) events from the control.


## -returns



This method returns S_OK in all cases.




## -remarks



The control is not required to stop sending events when <i>bFreeze</i> is <b>TRUE</b>. However, the container is not going to process them in this case. If a control depends on the container's processing -- as with request events that return information from the container -- the control must either discard the event or queue the event to send later when <i>bFreeze</i> is <b>FALSE</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
As with <a href="https://msdn.microsoft.com/9ca43723-a14e-4f03-8eec-e10ab34ecb4d">IOleControl::OnAmbientPropertyChange</a>, S_OK is returned in all cases in order to prevent a container from making assumptions about a control's behavior based on return values.




## -see-also




<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>
 

 

