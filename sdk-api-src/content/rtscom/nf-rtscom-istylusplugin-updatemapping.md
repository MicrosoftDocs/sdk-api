---
UID: NF:rtscom.IStylusPlugin.UpdateMapping
title: IStylusPlugin::UpdateMapping (rtscom.h)
description: Notifies the plug-in when display properties, such as dpi or orientation, change.
helpviewer_keywords: ["26cefb86-a21e-432d-b3db-1669d5b9cd05","IStylusPlugin interface [Tablet PC]","UpdateMapping method","IStylusPlugin.UpdateMapping","IStylusPlugin::UpdateMapping","UpdateMapping","UpdateMapping method [Tablet PC]","UpdateMapping method [Tablet PC]","IStylusPlugin interface","rtscom/IStylusPlugin::UpdateMapping","tablet.istylusplugin_updatemapping"]
old-location: tablet\istylusplugin_updatemapping.htm
tech.root: tablet
ms.assetid: 26cefb86-a21e-432d-b3db-1669d5b9cd05
ms.date: 12/05/2018
ms.keywords: 26cefb86-a21e-432d-b3db-1669d5b9cd05, IStylusPlugin interface [Tablet PC],UpdateMapping method, IStylusPlugin.UpdateMapping, IStylusPlugin::UpdateMapping, UpdateMapping, UpdateMapping method [Tablet PC], UpdateMapping method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::UpdateMapping, tablet.istylusplugin_updatemapping
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
 - IStylusPlugin::UpdateMapping
 - rtscom/IStylusPlugin::UpdateMapping
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
 - IStylusPlugin.UpdateMapping
---

# IStylusPlugin::UpdateMapping


## -description

Notifies the plug-in when display properties, such as dpi or orientation, change.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is called when display properties, such as dpi or orientation, change. Call the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getalltabletcontextids">IRealTimeStylus::GetAllTabletContextIds Method</a> method to get more information about the change.

The <b>IStylusPlugin::UpdateMapping Method</b> method provides a mechanism for applications to determine when tablet display properties change. This method is called on <a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a> messages.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-datainterest">IStylusPlugin::DataInterest Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>