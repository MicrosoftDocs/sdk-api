---
UID: NF:rtscom.IStylusPlugin.TabletRemoved
title: IStylusPlugin::TabletRemoved method
author: windows-driver-content
description: Notifies an implementing plug-in when an ITablet object is removed from the system.
old-location: tablet\istylusplugin_tabletremoved.htm
old-project: tablet
ms.assetid: b953c2f8-3f49-4b7a-af4a-528c8815b066
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IStylusPlugin, IStylusPlugin interface [Tablet PC], TabletRemoved method, IStylusPlugin::TabletRemoved, TabletRemoved method [Tablet PC], TabletRemoved method [Tablet PC], IStylusPlugin interface, TabletRemoved,IStylusPlugin.TabletRemoved, b953c2f8-3f49-4b7a-af4a-528c8815b066, rtscom/IStylusPlugin::TabletRemoved, tablet.istylusplugin_tabletremoved
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IStylusPlugin.TabletRemoved
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStylusPlugin::TabletRemoved method


## -description



Notifies an implementing plug-in when an <a href="https://msdn.microsoft.com/31e11f7d-5610-4c49-9203-2dc322fbef95">ITablet</a> object is removed from the system.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param iTabletIndex [in]

The tablet index.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called by the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object, whether the RTS object is enabled or disabled.




## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/fbc971ad-7cfb-4f75-8d63-a210a7967424">IStylusPlugin::TabletAdded Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

