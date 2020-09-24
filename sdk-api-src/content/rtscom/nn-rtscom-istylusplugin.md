---
UID: NN:rtscom.IStylusPlugin
title: IStylusPlugin (rtscom.h)
description: Receives notifications of RealTimeStylus Class events to enable you to perform custom processing based on those events.
helpviewer_keywords: ["IStylusPlugin","IStylusPlugin interface [Tablet PC]","IStylusPlugin interface [Tablet PC]","described","bbef5cdb-4112-4733-80bb-692b7a198605","rtscom/IStylusPlugin","tablet.istylusplugin"]
old-location: tablet\istylusplugin.htm
tech.root: tablet
ms.assetid: bbef5cdb-4112-4733-80bb-692b7a198605
ms.date: 12/05/2018
ms.keywords: IStylusPlugin, IStylusPlugin interface [Tablet PC], IStylusPlugin interface [Tablet PC],described, bbef5cdb-4112-4733-80bb-692b7a198605, rtscom/IStylusPlugin, tablet.istylusplugin
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
 - IStylusPlugin
 - rtscom/IStylusPlugin
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
 - IStylusPlugin
---

# IStylusPlugin interface


## -description

Receives notifications of <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> events to enable you to perform custom processing based on those events.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStylusPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStylusPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStylusPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-customstylusdataadded">CustomStylusDataAdded</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that custom stylus data is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-datainterest">DataInterest</a>
</td>
<td align="left" width="63%">
Represents the notifications a plug-in is to receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-error">Error</a>
</td>
<td align="left" width="63%">
Notifies the implementing object that this plug-in, one of the previous plug-ins in the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">StylusAsyncPlugin</a> collection, or a plug-in in the <b>StylusAsyncPlugin</b> collection threw an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-inairpackets">InAirPackets</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is moving above the digitizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">Packets</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is moving on the digitizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusdisabled">RealTimeStylusDisabled</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusenabled">RealTimeStylusEnabled</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusbuttondown">StylusButtonDown</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user is pressing a pen button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusbuttonup">StylusButtonUp</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user has released a pen button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">StylusDown</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen has touched the digitizer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusinrange">StylusInRange</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the tablet pen is entering the input area of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object or is entering the detection range of the digitizer above the input area of the <b>RealTimeStylus</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusoutofrange">StylusOutOfRange</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is leaving the input area of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object or is leaving the detection range of the digitizer above the input area of the <b>RealTimeStylus</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">StylusUp</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user has raised the pen from the tablet digitizer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-systemevent">SystemEvent</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in when a system event is received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-tabletadded">TabletAdded</a>
</td>
<td align="left" width="63%">
Notifies an implementing plug-in when an <a href="/windows/desktop/tablet/itablet">ITablet</a> object is attached to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-tabletremoved">TabletRemoved</a>
</td>
<td align="left" width="63%">
Notifies an implementing plug-in when an <a href="/windows/desktop/tablet/itablet">ITablet</a> object is removed from the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-updatemapping">UpdateMapping</a>
</td>
<td align="left" width="63%">
Notifies the implementing object when tablet display properties have changed.

</td>
</tr>
</table>

## -remarks

Both the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> and <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interfaces derive from this interface and can be added to <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> plug-in collections.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>