---
UID: NF:rtscom.IStylusPlugin.TabletRemoved
title: IStylusPlugin::TabletRemoved (rtscom.h)
description: Notifies an implementing plug-in when an ITablet object is removed from the system.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","TabletRemoved method","IStylusPlugin.TabletRemoved","IStylusPlugin::TabletRemoved","TabletRemoved","TabletRemoved method [Tablet PC]","TabletRemoved method [Tablet PC]","IStylusPlugin interface","b953c2f8-3f49-4b7a-af4a-528c8815b066","rtscom/IStylusPlugin::TabletRemoved","tablet.istylusplugin_tabletremoved"]
old-location: tablet\istylusplugin_tabletremoved.htm
tech.root: tablet
ms.assetid: b953c2f8-3f49-4b7a-af4a-528c8815b066
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],TabletRemoved method, IStylusPlugin.TabletRemoved, IStylusPlugin::TabletRemoved, TabletRemoved, TabletRemoved method [Tablet PC], TabletRemoved method [Tablet PC],IStylusPlugin interface, b953c2f8-3f49-4b7a-af4a-528c8815b066, rtscom/IStylusPlugin::TabletRemoved, tablet.istylusplugin_tabletremoved
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
 - IStylusPlugin::TabletRemoved
 - rtscom/IStylusPlugin::TabletRemoved
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
 - IStylusPlugin.TabletRemoved
---

# IStylusPlugin::TabletRemoved


## -description

Notifies an implementing plug-in when an <a href="/windows/desktop/tablet/itablet">ITablet</a> object is removed from the system.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.

### -param iTabletIndex [in]

The tablet index.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is called by the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object, whether the RTS object is enabled or disabled.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-tabletadded">IStylusPlugin::TabletAdded Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>