---
UID: NF:rtscom.IStylusPlugin.TabletAdded
title: IStylusPlugin::TabletAdded (rtscom.h)
description: Notifies an implementing plug-in when an ITablet object is attached to the system.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","TabletAdded method","IStylusPlugin.TabletAdded","IStylusPlugin::TabletAdded","TabletAdded","TabletAdded method [Tablet PC]","TabletAdded method [Tablet PC]","IStylusPlugin interface","fbc971ad-7cfb-4f75-8d63-a210a7967424","rtscom/IStylusPlugin::TabletAdded","tablet.istylusplugin_tabletadded"]
old-location: tablet\istylusplugin_tabletadded.htm
tech.root: tablet
ms.assetid: fbc971ad-7cfb-4f75-8d63-a210a7967424
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],TabletAdded method, IStylusPlugin.TabletAdded, IStylusPlugin::TabletAdded, TabletAdded, TabletAdded method [Tablet PC], TabletAdded method [Tablet PC],IStylusPlugin interface, fbc971ad-7cfb-4f75-8d63-a210a7967424, rtscom/IStylusPlugin::TabletAdded, tablet.istylusplugin_tabletadded
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
 - IStylusPlugin::TabletAdded
 - rtscom/IStylusPlugin::TabletAdded
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
 - IStylusPlugin.TabletAdded
---

# IStylusPlugin::TabletAdded


## -description

Notifies an implementing plug-in when an <a href="/windows/desktop/tablet/itablet">ITablet</a> object is attached to the system.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param piTablet [in]

 The added tablet object.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is called by the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object, whether the <b>RealTimeStylus Class</b> object is enabled or disabled.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-tabletremoved">IStylusPlugin::TabletRemoved Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>