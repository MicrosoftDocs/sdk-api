---
UID: NF:rtscom.IStylusPlugin.UpdateMapping
title: IStylusPlugin::UpdateMapping
author: windows-sdk-content
description: Notifies the plug-in when display properties, such as dpi or orientation, change.
old-location: tablet\istylusplugin_updatemapping.htm
tech.root: tablet
ms.assetid: 26cefb86-a21e-432d-b3db-1669d5b9cd05
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 26cefb86-a21e-432d-b3db-1669d5b9cd05, IStylusPlugin interface [Tablet PC],UpdateMapping method, IStylusPlugin.UpdateMapping, IStylusPlugin::UpdateMapping, UpdateMapping, UpdateMapping method [Tablet PC], UpdateMapping method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::UpdateMapping, tablet.istylusplugin_updatemapping
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
 - IStylusPlugin.UpdateMapping
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
- IStylusPlugin.UpdateMapping
: 
---

# IStylusPlugin::UpdateMapping


## -description



Notifies the plug-in when display properties, such as dpi or orientation, change.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called when display properties, such as dpi or orientation, change. Call the <a href="https://msdn.microsoft.com/1fac0624-2e1c-44b2-8a11-82b746a18356">IRealTimeStylus::GetAllTabletContextIds Method</a> method to get more information about the change.

The <b>IStylusPlugin::UpdateMapping Method</b> method provides a mechanism for applications to determine when tablet display properties change. This method is called on <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/7ff6ccf2-292c-4321-be2a-d6db7ce14943">IStylusPlugin::DataInterest Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

