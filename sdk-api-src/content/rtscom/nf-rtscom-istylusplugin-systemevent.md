---
UID: NF:rtscom.IStylusPlugin.SystemEvent
title: IStylusPlugin::SystemEvent (rtscom.h)
author: windows-sdk-content
description: Notifies the implementing plug-in that a system event is available.
old-location: tablet\istylusplugin_systemevent.htm
tech.root: tablet
ms.assetid: 7cdba29e-0599-45f7-8853-3e8fa29897e8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7cdba29e-0599-45f7-8853-3e8fa29897e8, IStylusPlugin interface [Tablet PC],SystemEvent method, IStylusPlugin.SystemEvent, IStylusPlugin::SystemEvent, SystemEvent, SystemEvent method [Tablet PC], SystemEvent method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::SystemEvent, tablet.istylusplugin_systemevent
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
ms.custom: 19H1
---

# IStylusPlugin::SystemEvent


## -description



Notifies the implementing plug-in that a system event is available.




## -parameters




### -param piRtsSrc [in]

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param tcid [in]

The tablet context identifier for the event.


### -param sid [in]

The security identifier.


### -param event [in]

The system event sent by the RTS object


### -param eventdata [in]

The 
              <a href="https://docs.microsoft.com/windows/desktop/api/tpcshrd/ns-tpcshrd-tagsystem_event_data">SYSTEM_EVENT_DATA</a> structure containing information about the system event, <i>event</i>.


## -returns



For a description of return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/classes-and-interfaces---ink-analysis">Classes and Interfaces - Ink Analysis</a>.




## -remarks



When a system event is being processed the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object provides real time stylus events on a specific window handle within a specific window input rectangle.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getdesiredpacketdescription">IRealTimeStylus::GetDesiredPacketDescription Method</a> method to determine what packet properties are sent in the events.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_windowinputrectangle">IRealTimeStylus::WindowInputRectangle Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-datainterest">IStylusPlugin::DataInterest Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>
 

 

