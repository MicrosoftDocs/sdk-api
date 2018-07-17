---
UID: NF:rtscom.IStylusPlugin.StylusOutOfRange
title: IStylusPlugin::StylusOutOfRange
author: windows-sdk-content
description: Notifies the implementing plug-in that the stylus has left the detection range of the digitizer.
old-location: tablet\istylusplugin_stylusoutofrange.htm
old-project: tablet
ms.assetid: fd662c32-c226-4dbb-807a-3e560452ef15
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IStylusPlugin interface [Tablet PC],StylusOutOfRange method, IStylusPlugin.StylusOutOfRange, IStylusPlugin::StylusOutOfRange, StylusOutOfRange, StylusOutOfRange method [Tablet PC], StylusOutOfRange method [Tablet PC],IStylusPlugin interface, fd662c32-c226-4dbb-807a-3e560452ef15, rtscom/IStylusPlugin::StylusOutOfRange, tablet.istylusplugin_stylusoutofrange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.StylusOutOfRange
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IStylusPlugin::StylusOutOfRange


## -description



Notifies the implementing plug-in that the stylus has left the detection range of the digitizer.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param tcid [in]

Tablet context identifier.


### -param sid [in]

Stylus identifier.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The stylus is out of range of the digitizer.




## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

