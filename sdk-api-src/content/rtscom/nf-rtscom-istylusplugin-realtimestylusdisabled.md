---
UID: NF:rtscom.IStylusPlugin.RealTimeStylusDisabled
title: IStylusPlugin::RealTimeStylusDisabled
author: windows-sdk-content
description: Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is disabled.
old-location: tablet\istylusplugin_realtimestylusdisabled.htm
tech.root: tablet
ms.assetid: 62425c21-62fb-4a29-b024-8d5dc237b430
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 62425c21-62fb-4a29-b024-8d5dc237b430, IStylusPlugin interface [Tablet PC],RealTimeStylusDisabled method, IStylusPlugin.RealTimeStylusDisabled, IStylusPlugin::RealTimeStylusDisabled, RealTimeStylusDisabled, RealTimeStylusDisabled method [Tablet PC], RealTimeStylusDisabled method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::RealTimeStylusDisabled, tablet.istylusplugin_realtimestylusdisabled
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
 - IStylusPlugin.RealTimeStylusDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusPlugin::RealTimeStylusDisabled


## -description



Notifies the implementing plug-in that the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object is disabled.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param cTcidCount [in]

Number of tablet context identifiers the RTS has encountered. Valid values are 0 through 8, inclusive.


### -param pTcids [in]

The tablet context identifiers.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called when the RTS object has been disabled, or when a plug-in is removed from a collection.




## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

