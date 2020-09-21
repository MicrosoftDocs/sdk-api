---
UID: NF:rtscom.IRealTimeStylus.GetStylusAsyncPlugin
title: IRealTimeStylus::GetStylusAsyncPlugin (rtscom.h)
description: Retrieves the plug-in at the specified index in the asynchronous plug-in collection.
helpviewer_keywords: ["229e14f6-e0b1-40e0-a58e-daf1ba08cd1f","GetStylusAsyncPlugin","GetStylusAsyncPlugin method [Tablet PC]","GetStylusAsyncPlugin method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetStylusAsyncPlugin method","IRealTimeStylus.GetStylusAsyncPlugin","IRealTimeStylus::GetStylusAsyncPlugin","rtscom/IRealTimeStylus::GetStylusAsyncPlugin","tablet.irealtimestylus_getstylusasyncplugin"]
old-location: tablet\irealtimestylus_getstylusasyncplugin.htm
tech.root: tablet
ms.assetid: 229e14f6-e0b1-40e0-a58e-daf1ba08cd1f
ms.date: 12/05/2018
ms.keywords: 229e14f6-e0b1-40e0-a58e-daf1ba08cd1f, GetStylusAsyncPlugin, GetStylusAsyncPlugin method [Tablet PC], GetStylusAsyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStylusAsyncPlugin method, IRealTimeStylus.GetStylusAsyncPlugin, IRealTimeStylus::GetStylusAsyncPlugin, rtscom/IRealTimeStylus::GetStylusAsyncPlugin, tablet.irealtimestylus_getstylusasyncplugin
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
 - IRealTimeStylus::GetStylusAsyncPlugin
 - rtscom/IRealTimeStylus::GetStylusAsyncPlugin
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
 - IRealTimeStylus.GetStylusAsyncPlugin
---

# IRealTimeStylus::GetStylusAsyncPlugin


## -description

Retrieves the plug-in at the specified index in the asynchronous plug-in collection.

## -parameters

### -param iIndex [in]

The index for the plug-in that is in the asynchronous plug-in collection.

### -param ppiPlugin [out]

 A pointer to the plug-in.

## -returns

For a description of the return values see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusasyncplugincount">IRealTimeStylus::GetStylusAsyncPluginCount Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>