---
UID: NF:rtscom.IStylusPlugin.StylusOutOfRange
title: IStylusPlugin::StylusOutOfRange (rtscom.h)
description: Notifies the implementing plug-in that the stylus has left the detection range of the digitizer.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","StylusOutOfRange method","IStylusPlugin.StylusOutOfRange","IStylusPlugin::StylusOutOfRange","StylusOutOfRange","StylusOutOfRange method [Tablet PC]","StylusOutOfRange method [Tablet PC]","IStylusPlugin interface","fd662c32-c226-4dbb-807a-3e560452ef15","rtscom/IStylusPlugin::StylusOutOfRange","tablet.istylusplugin_stylusoutofrange"]
old-location: tablet\istylusplugin_stylusoutofrange.htm
tech.root: tablet
ms.assetid: fd662c32-c226-4dbb-807a-3e560452ef15
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],StylusOutOfRange method, IStylusPlugin.StylusOutOfRange, IStylusPlugin::StylusOutOfRange, StylusOutOfRange, StylusOutOfRange method [Tablet PC], StylusOutOfRange method [Tablet PC],IStylusPlugin interface, fd662c32-c226-4dbb-807a-3e560452ef15, rtscom/IStylusPlugin::StylusOutOfRange, tablet.istylusplugin_stylusoutofrange
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
 - IStylusPlugin::StylusOutOfRange
 - rtscom/IStylusPlugin::StylusOutOfRange
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
 - IStylusPlugin.StylusOutOfRange
---

# IStylusPlugin::StylusOutOfRange


## -description

Notifies the implementing plug-in that the stylus has left the detection range of the digitizer.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param tcid [in]

Tablet context identifier.

### -param sid [in]

Stylus identifier.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The stylus is out of range of the digitizer.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>