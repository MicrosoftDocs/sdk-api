---
UID: NF:rtscom.IStylusPlugin.TabletAdded
title: IStylusPlugin::TabletAdded
author: windows-sdk-content
description: Notifies an implementing plug-in when an ITablet object is attached to the system.
old-location: tablet\istylusplugin_tabletadded.htm
tech.root: tablet
ms.assetid: fbc971ad-7cfb-4f75-8d63-a210a7967424
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStylusPlugin interface [Tablet PC],TabletAdded method, IStylusPlugin.TabletAdded, IStylusPlugin::TabletAdded, TabletAdded, TabletAdded method [Tablet PC], TabletAdded method [Tablet PC],IStylusPlugin interface, fbc971ad-7cfb-4f75-8d63-a210a7967424, rtscom/IStylusPlugin::TabletAdded, tablet.istylusplugin_tabletadded
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
 - IStylusPlugin.TabletAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusPlugin::TabletAdded


## -description



Notifies an implementing plug-in when an <a href="https://msdn.microsoft.com/31e11f7d-5610-4c49-9203-2dc322fbef95">ITablet</a> object is attached to the system.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param piTablet [in]

 The added tablet object.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called by the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object, whether the <b>RealTimeStylus Class</b> object is enabled or disabled.




## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/b953c2f8-3f49-4b7a-af4a-528c8815b066">IStylusPlugin::TabletRemoved Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

