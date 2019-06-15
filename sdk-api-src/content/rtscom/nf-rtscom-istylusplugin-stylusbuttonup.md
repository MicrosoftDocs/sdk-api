---
UID: NF:rtscom.IStylusPlugin.StylusButtonUp
title: IStylusPlugin::StylusButtonUp (rtscom.h)
author: windows-sdk-content
description: Notifies the implementing plug-in that the user has released a stylus button.
old-location: tablet\istylusplugin_stylusbuttonup.htm
tech.root: tablet
ms.assetid: a56182f3-3e9a-4cc2-895d-54010cd00cb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],StylusButtonUp method, IStylusPlugin.StylusButtonUp, IStylusPlugin::StylusButtonUp, StylusButtonUp, StylusButtonUp method [Tablet PC], StylusButtonUp method [Tablet PC],IStylusPlugin interface, a56182f3-3e9a-4cc2-895d-54010cd00cb4, rtscom/IStylusPlugin::StylusButtonUp, tablet.istylusplugin_stylusbuttonup
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
ms.custom: 19H1
---

# IStylusPlugin::StylusButtonUp


## -description



Notifies the implementing plug-in that the user has released a stylus button.




## -parameters




### -param piRtsSrc [in]

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param sid [in]

Security identifier.


### -param pGuidStylusButton [in]

The globally unique identifier (GUID) for the stylus button data.


### -param pStylusPos [in, out]

A<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/ns-rtscom-stylusinfo">StylusInfo Structure</a> containing the information about the RTS that is associated with the stylus.


## -returns



For a description of return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The stylus button is no longer down and the stylus is in range of the digitizer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusbuttondown">IStylusPlugin::StylusButtonDown Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>
 

 

