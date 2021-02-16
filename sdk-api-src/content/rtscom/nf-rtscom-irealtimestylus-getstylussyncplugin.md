---
UID: NF:rtscom.IRealTimeStylus.GetStylusSyncPlugin
title: IRealTimeStylus::GetStylusSyncPlugin (rtscom.h)
description: Retrieves the plug-in at the specified index in the synchronous plug-in collection.
helpviewer_keywords: ["GetStylusSyncPlugin","GetStylusSyncPlugin method [Tablet PC]","GetStylusSyncPlugin method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetStylusSyncPlugin method","IRealTimeStylus.GetStylusSyncPlugin","IRealTimeStylus::GetStylusSyncPlugin","ec587954-cf7c-4f2d-a20d-b401011f7140","rtscom/IRealTimeStylus::GetStylusSyncPlugin","tablet.irealtimestylus_getstylussyncplugin"]
old-location: tablet\irealtimestylus_getstylussyncplugin.htm
tech.root: tablet
ms.assetid: ec587954-cf7c-4f2d-a20d-b401011f7140
ms.date: 12/05/2018
ms.keywords: GetStylusSyncPlugin, GetStylusSyncPlugin method [Tablet PC], GetStylusSyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStylusSyncPlugin method, IRealTimeStylus.GetStylusSyncPlugin, IRealTimeStylus::GetStylusSyncPlugin, ec587954-cf7c-4f2d-a20d-b401011f7140, rtscom/IRealTimeStylus::GetStylusSyncPlugin, tablet.irealtimestylus_getstylussyncplugin
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
 - IRealTimeStylus::GetStylusSyncPlugin
 - rtscom/IRealTimeStylus::GetStylusSyncPlugin
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
 - IRealTimeStylus.GetStylusSyncPlugin
---

# IRealTimeStylus::GetStylusSyncPlugin


## -description

Retrieves the plug-in at the specified index in the synchronous plug-in collection.

## -parameters

### -param iIndex [in]

The index for the plug-in that is in the synchronous plug-in collection.

### -param ppiPlugin [out]

A pointer to  the plug-in.

## -returns

For a description of the return values see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylussyncplugincount">IRealTimeStylus::GetStylusSyncPluginCount Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>