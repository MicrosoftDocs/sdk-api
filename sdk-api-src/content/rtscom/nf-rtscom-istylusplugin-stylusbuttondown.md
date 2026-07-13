---
UID: NF:rtscom.IStylusPlugin.StylusButtonDown
title: IStylusPlugin::StylusButtonDown (rtscom.h)
description: Notifies the implementing plug-in that the user is pressing a stylus button.
helpviewer_keywords: ["60cd2b46-14f7-4a06-a1e7-5b2aa9a1f05c","IStylusPlugin interface [Tablet PC]","StylusButtonDown method","IStylusPlugin.StylusButtonDown","IStylusPlugin::StylusButtonDown","StylusButtonDown","StylusButtonDown method [Tablet PC]","StylusButtonDown method [Tablet PC]","IStylusPlugin interface","rtscom/IStylusPlugin::StylusButtonDown","tablet.istylusplugin_stylusbuttondown"]
old-location: tablet\istylusplugin_stylusbuttondown.htm
tech.root: tablet
ms.assetid: 60cd2b46-14f7-4a06-a1e7-5b2aa9a1f05c
ms.date: 12/05/2018
ms.keywords: 60cd2b46-14f7-4a06-a1e7-5b2aa9a1f05c, IStylusPlugin interface [Tablet PC],StylusButtonDown method, IStylusPlugin.StylusButtonDown, IStylusPlugin::StylusButtonDown, StylusButtonDown, StylusButtonDown method [Tablet PC], StylusButtonDown method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::StylusButtonDown, tablet.istylusplugin_stylusbuttondown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStylusPlugin::StylusButtonDown
 - rtscom/IStylusPlugin::StylusButtonDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.StylusButtonDown
---

# IStylusPlugin::StylusButtonDown


## -description

Notifies the implementing plug-in that the user is pressing a stylus button.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param sid [in]

Security identifier.

### -param pGuidStylusButton [in]

The GUID-type identifier for the stylus button data. The GUID indicates the unique identifier for this data object.

### -param pStylusPos [in, out]

A <a href="/windows/desktop/api/rtscom/ns-rtscom-stylusinfo">StylusInfo Structure</a> containing the information about the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that is associated with the stylus.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This notification is used to when the stylus button is down and the stylus is in range of the digitizer.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>