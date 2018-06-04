---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

