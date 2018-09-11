---
UID: NF:rtscom.IStylusPlugin.StylusButtonUp
title: IStylusPlugin::StylusButtonUp
author: windows-sdk-content
description: Notifies the implementing plug-in that the user has released a stylus button.
old-location: tablet\istylusplugin_stylusbuttonup.htm
tech.root: tablet
ms.assetid: a56182f3-3e9a-4cc2-895d-54010cd00cb4
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IStylusPlugin interface [Tablet PC],StylusButtonUp method, IStylusPlugin.StylusButtonUp, IStylusPlugin::StylusButtonUp, StylusButtonUp, StylusButtonUp method [Tablet PC], StylusButtonUp method [Tablet PC],IStylusPlugin interface, a56182f3-3e9a-4cc2-895d-54010cd00cb4, rtscom/IStylusPlugin::StylusButtonUp, tablet.istylusplugin_stylusbuttonup
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
 - IStylusPlugin.StylusButtonUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusPlugin::StylusButtonUp


## -description



Notifies the implementing plug-in that the user has released a stylus button.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param sid [in]

Security identifier.


### -param pGuidStylusButton [in]

The globally unique identifier (GUID) for the stylus button data.


### -param pStylusPos [in, out]

A<a href="https://msdn.microsoft.com/d2642082-e18c-4f91-b08c-e25aa388a2a3">StylusInfo Structure</a> containing the information about the RTS that is associated with the stylus.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The stylus button is no longer down and the stylus is in range of the digitizer.




## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/60cd2b46-14f7-4a06-a1e7-5b2aa9a1f05c">IStylusPlugin::StylusButtonDown Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

