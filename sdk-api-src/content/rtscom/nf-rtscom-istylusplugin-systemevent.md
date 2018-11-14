---
UID: NF:rtscom.IStylusPlugin.SystemEvent
title: IStylusPlugin::SystemEvent
author: windows-sdk-content
description: Notifies the implementing plug-in that a system event is available.
old-location: tablet\istylusplugin_systemevent.htm
tech.root: tablet
ms.assetid: 7cdba29e-0599-45f7-8853-3e8fa29897e8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 7cdba29e-0599-45f7-8853-3e8fa29897e8, IStylusPlugin interface [Tablet PC],SystemEvent method, IStylusPlugin.SystemEvent, IStylusPlugin::SystemEvent, SystemEvent, SystemEvent method [Tablet PC], SystemEvent method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::SystemEvent, tablet.istylusplugin_systemevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.SystemEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rtscom.h
: 
- IStylusPlugin.SystemEvent
: 
---

# IStylusPlugin::SystemEvent


## -description



Notifies the implementing plug-in that a system event is available.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param tcid [in]

The tablet context identifier for the event.


### -param sid [in]

The security identifier.


### -param event [in]

The system event sent by the RTS object


### -param eventdata [in]

The 
              <a href="https://msdn.microsoft.com/3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90">SYSTEM_EVENT_DATA</a> structure containing information about the system event, <i>event</i>.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/712908e1-2d1d-4e42-8c80-71354b03d318">Classes and Interfaces - Ink Analysis</a>.




## -remarks



When a system event is being processed the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object provides real time stylus events on a specific window handle within a specific window input rectangle.

Use the <a href="https://msdn.microsoft.com/8799eb17-8ad0-49c1-a278-40b3bff9d281">IRealTimeStylus::GetDesiredPacketDescription Method</a> method to determine what packet properties are sent in the events.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/e202be43-48c7-4fa4-b049-efdda3ef2ada">IRealTimeStylus::WindowInputRectangle Property</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/7ff6ccf2-292c-4321-be2a-d6db7ce14943">IStylusPlugin::DataInterest Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

