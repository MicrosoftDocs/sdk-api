---
UID: NF:rtscom.IStylusPlugin.RealTimeStylusDisabled
title: IStylusPlugin::RealTimeStylusDisabled (rtscom.h)
description: Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is disabled.
helpviewer_keywords: ["62425c21-62fb-4a29-b024-8d5dc237b430","IStylusPlugin interface [Tablet PC]","RealTimeStylusDisabled method","IStylusPlugin.RealTimeStylusDisabled","IStylusPlugin::RealTimeStylusDisabled","RealTimeStylusDisabled","RealTimeStylusDisabled method [Tablet PC]","RealTimeStylusDisabled method [Tablet PC]","IStylusPlugin interface","rtscom/IStylusPlugin::RealTimeStylusDisabled","tablet.istylusplugin_realtimestylusdisabled"]
old-location: tablet\istylusplugin_realtimestylusdisabled.htm
tech.root: tablet
ms.assetid: 62425c21-62fb-4a29-b024-8d5dc237b430
ms.date: 12/05/2018
ms.keywords: 62425c21-62fb-4a29-b024-8d5dc237b430, IStylusPlugin interface [Tablet PC],RealTimeStylusDisabled method, IStylusPlugin.RealTimeStylusDisabled, IStylusPlugin::RealTimeStylusDisabled, RealTimeStylusDisabled, RealTimeStylusDisabled method [Tablet PC], RealTimeStylusDisabled method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::RealTimeStylusDisabled, tablet.istylusplugin_realtimestylusdisabled
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
 - IStylusPlugin::RealTimeStylusDisabled
 - rtscom/IStylusPlugin::RealTimeStylusDisabled
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
 - IStylusPlugin.RealTimeStylusDisabled
---

# IStylusPlugin::RealTimeStylusDisabled


## -description

Notifies the implementing plug-in that the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object is disabled.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param cTcidCount [in]

Number of tablet context identifiers the RTS has encountered. Valid values are 0 through 8, inclusive.

### -param pTcids [in]

The tablet context identifiers.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is called when the RTS object has been disabled, or when a plug-in is removed from a collection.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>