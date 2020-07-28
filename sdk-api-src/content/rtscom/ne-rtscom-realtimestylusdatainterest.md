---
UID: NE:rtscom.RealTimeStylusDataInterest
title: RealTimeStylusDataInterest (rtscom.h)
description: Defines the values used by plug-ins to specify which event notifications the plug-ins receive.
helpviewer_keywords: ["RTSDI_AllData","RTSDI_CustomStylusDataAdded","RTSDI_DefaultEvents","RTSDI_Error","RTSDI_InAirPackets","RTSDI_None","RTSDI_Packets","RTSDI_RealTimeStylusDisabled","RTSDI_RealTimeStylusEnabled","RTSDI_StylusButtonDown","RTSDI_StylusButtonUp","RTSDI_StylusDown","RTSDI_StylusInRange","RTSDI_StylusNew","RTSDI_StylusOutOfRange","RTSDI_StylusUp","RTSDI_SystemEvents","RTSDI_TabletAdded","RTSDI_TabletRemoved","RTSDI_UpdateMapping","RealTimeStylusDataInterest","RealTimeStylusDataInterest enumeration [Tablet PC]","f50cfafb-e709-4819-9e1a-679fbb54c7e0","rtscom/RTSDI_AllData","rtscom/RTSDI_CustomStylusDataAdded","rtscom/RTSDI_DefaultEvents","rtscom/RTSDI_Error","rtscom/RTSDI_InAirPackets","rtscom/RTSDI_None","rtscom/RTSDI_Packets","rtscom/RTSDI_RealTimeStylusDisabled","rtscom/RTSDI_RealTimeStylusEnabled","rtscom/RTSDI_StylusButtonDown","rtscom/RTSDI_StylusButtonUp","rtscom/RTSDI_StylusDown","rtscom/RTSDI_StylusInRange","rtscom/RTSDI_StylusNew","rtscom/RTSDI_StylusOutOfRange","rtscom/RTSDI_StylusUp","rtscom/RTSDI_SystemEvents","rtscom/RTSDI_TabletAdded","rtscom/RTSDI_TabletRemoved","rtscom/RTSDI_UpdateMapping","rtscom/RealTimeStylusDataInterest","tablet.realtimestylusdatainterest"]
old-location: tablet\realtimestylusdatainterest.htm
tech.root: tablet
ms.assetid: f50cfafb-e709-4819-9e1a-679fbb54c7e0
ms.date: 12/05/2018
ms.keywords: RTSDI_AllData, RTSDI_CustomStylusDataAdded, RTSDI_DefaultEvents, RTSDI_Error, RTSDI_InAirPackets, RTSDI_None, RTSDI_Packets, RTSDI_RealTimeStylusDisabled, RTSDI_RealTimeStylusEnabled, RTSDI_StylusButtonDown, RTSDI_StylusButtonUp, RTSDI_StylusDown, RTSDI_StylusInRange, RTSDI_StylusNew, RTSDI_StylusOutOfRange, RTSDI_StylusUp, RTSDI_SystemEvents, RTSDI_TabletAdded, RTSDI_TabletRemoved, RTSDI_UpdateMapping, RealTimeStylusDataInterest, RealTimeStylusDataInterest enumeration [Tablet PC], f50cfafb-e709-4819-9e1a-679fbb54c7e0, rtscom/RTSDI_AllData, rtscom/RTSDI_CustomStylusDataAdded, rtscom/RTSDI_DefaultEvents, rtscom/RTSDI_Error, rtscom/RTSDI_InAirPackets, rtscom/RTSDI_None, rtscom/RTSDI_Packets, rtscom/RTSDI_RealTimeStylusDisabled, rtscom/RTSDI_RealTimeStylusEnabled, rtscom/RTSDI_StylusButtonDown, rtscom/RTSDI_StylusButtonUp, rtscom/RTSDI_StylusDown, rtscom/RTSDI_StylusInRange, rtscom/RTSDI_StylusNew, rtscom/RTSDI_StylusOutOfRange, rtscom/RTSDI_StylusUp, rtscom/RTSDI_SystemEvents, rtscom/RTSDI_TabletAdded, rtscom/RTSDI_TabletRemoved, rtscom/RTSDI_UpdateMapping, rtscom/RealTimeStylusDataInterest, tablet.realtimestylusdatainterest
f1_keywords:
- rtscom/RealTimeStylusDataInterest
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- RTSCom.h
api_name:
- RealTimeStylusDataInterest
targetos: Windows
req.typenames: RealTimeStylusDataInterest
req.redist: 
ms.custom: 19H1
---

# RealTimeStylusDataInterest enumeration


## -description



Defines the values used by plug-ins to specify which event notifications the plug-ins receive.




## -enum-fields




### -field RTSDI_AllData

The plug-in receives notifications for all stylus data.


### -field RTSDI_None

The plug-in receives no notifications for any stylus data.


### -field RTSDI_Error

An error has been added to the input queue.


### -field RTSDI_RealTimeStylusEnabled

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has been enabled.


### -field RTSDI_RealTimeStylusDisabled

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has been disabled.


### -field RTSDI_StylusNew

A <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object encounters a new Stylus object.


### -field RTSDI_StylusInRange

The Stylus object is in range of the digitizer. Notifies the implementing plug-in that the stylus is entering the input area of the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object or is entering the detection range of the digitizer above the input area of the <b>RealTimeStylus Class</b> object.


### -field RTSDI_InAirPackets

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is within range of, but not touching, the digitizer and is moving.


### -field RTSDI_StylusOutOfRange

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is out of range of the digitizer. Informs the implementing plug-in that the stylus is leaving the input area of the <b>RealTimeStylus Class</b> object or is leaving the detection range of the digitizer above the input area of the <b>RealTimeStylus Class</b> object.


### -field RTSDI_StylusDown

The stylus is in contact with the digitizer.


### -field RTSDI_Packets

The stylus is moving and is in contact with the digitizer.


### -field RTSDI_StylusUp

The stylus has broken physical contact with the digitizer.


### -field RTSDI_StylusButtonUp

A user has realeased a stylus button.


### -field RTSDI_StylusButtonDown

A user has pressed  a stylus button.


### -field RTSDI_SystemEvents

A system event has been detected.


### -field RTSDI_TabletAdded

A new tablet device has been detected by the system. Notifies the implementing plug-in when a Microsoft.Ink.Tablet object is added to the system.


### -field RTSDI_TabletRemoved

A tablet device has been removed from the system. Notifies the implementing plug-in when a Microsoft.Ink.Tablet object is removed from the system.


### -field RTSDI_CustomStylusDataAdded

A plug-in has added data to a queue. You can identify the kind of custom data by either the GUID or Type.


### -field RTSDI_UpdateMapping

A tablet mapping to the screen has been changed or set.


### -field RTSDI_DefaultEvents

The plug-in receives the default stylus data.


## -remarks



The <b>RealTimeStylusDataInterest Enumeration</b> values are used in a bitwise combination that defines the set of data notifications. Use the <b>RealTimeStylusDataInterest Enumeration</b> to specify only the events for which you would like to receive notification. Thus, improving performance.

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> notifies plug-ins when it is retrieving packet data by calling into the respective plug-ins in a specified sequence. You control the sequence and types of plug-ins that receive these notifications. The packet data in the events can be modified by the plug-ins the <b>RealTimeStylus Class</b> object calls into.

You can control which methods are called on your plug-in by implementing the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>:: <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-datainterest">IStylusPlugin::DataInterest Method</a> method.

The following events are the default events:

<ul>
<li>RTSDI_RealTimeStylusEnabled</li>
<li>RTSDI_RealTimeStylusDisabled</li>
<li>RTSDI_StylusDown</li>
<li>RTSDI_Packets</li>
<li>RTSDI_StylusUp</li>
<li>RTSDI_SystemEvents</li>
<li>RTSDI_CustomStylusDataAdded</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
 

 

