---
UID: NF:rtscom.IRealTimeStylus.get_ChildRealTimeStylusPlugin
title: IRealTimeStylus::get_ChildRealTimeStylusPlugin (rtscom.h)
description: Gets or sets a RealTimeStylus object as an asynchronous plug-in of the current RealTimeStylus object.
helpviewer_keywords: ["269c133c-6950-40e0-8de9-e38bfa06995e","ChildRealTimeStylusPlugin property [Tablet PC]","ChildRealTimeStylusPlugin property [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","ChildRealTimeStylusPlugin property","IRealTimeStylus.ChildRealTimeStylusPlugin","IRealTimeStylus.get_ChildRealTimeStylusPlugin","IRealTimeStylus.put_ChildRealTimeStylusPlugin","IRealTimeStylus::ChildRealTimeStylusPlugin","IRealTimeStylus::get_ChildRealTimeStylusPlugin","IRealTimeStylus::put_ChildRealTimeStylusPlugin","get_ChildRealTimeStylusPlugin","rtscom/IRealTimeStylus::ChildRealTimeStylusPlugin","rtscom/IRealTimeStylus::get_ChildRealTimeStylusPlugin","rtscom/IRealTimeStylus::put_ChildRealTimeStylusPlugin","tablet.irealtimestylus_childrealtimestylusplugin"]
old-location: tablet\irealtimestylus_childrealtimestylusplugin.htm
tech.root: tablet
ms.assetid: 269c133c-6950-40e0-8de9-e38bfa06995e
ms.date: 12/05/2018
ms.keywords: 269c133c-6950-40e0-8de9-e38bfa06995e, ChildRealTimeStylusPlugin property [Tablet PC], ChildRealTimeStylusPlugin property [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],ChildRealTimeStylusPlugin property, IRealTimeStylus.ChildRealTimeStylusPlugin, IRealTimeStylus.get_ChildRealTimeStylusPlugin, IRealTimeStylus.put_ChildRealTimeStylusPlugin, IRealTimeStylus::ChildRealTimeStylusPlugin, IRealTimeStylus::get_ChildRealTimeStylusPlugin, IRealTimeStylus::put_ChildRealTimeStylusPlugin, get_ChildRealTimeStylusPlugin, rtscom/IRealTimeStylus::ChildRealTimeStylusPlugin, rtscom/IRealTimeStylus::get_ChildRealTimeStylusPlugin, rtscom/IRealTimeStylus::put_ChildRealTimeStylusPlugin, tablet.irealtimestylus_childrealtimestylusplugin
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
 - IRealTimeStylus::get_ChildRealTimeStylusPlugin
 - rtscom/IRealTimeStylus::get_ChildRealTimeStylusPlugin
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
 - IRealTimeStylus.ChildRealTimeStylusPlugin
 - IRealTimeStylus.get_ChildRealTimeStylusPlugin
 - IRealTimeStylus.put_ChildRealTimeStylusPlugin
 - IRealTimeStylus.get_ChildRealTimeStylusPlugin
 - IRealTimeStylus.put_ChildRealTimeStylusPlugin
---

# IRealTimeStylus::get_ChildRealTimeStylusPlugin


## -description

Gets or sets a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object as an asynchronous plug-in of the current <b>RealTimeStylus</b> object.



This property is read/write.

## -parameters

## -remarks

If there is no child RTS, getting the property returns S_OK with the <i>ppiRTS</i> parameter set to <b>NULL</b>. Setting the child RTS property to <b>NULL</b> breaks the cascade.

<div class="alert"><b>Note</b>  If there is no child RTS, setting the property to <b>NULL</b> returns S_OK.</div>
<div> </div>
A child <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> cannot have another cascaded child <b>RealTimeStylus</b>.

Plug-ins in the asynchronous collection cannot have children.

If a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object is set as a child by using the <b>IRealTimeStylus::ChildRealTimeStylusPlugin Property</b> property, no other asynchronous plug-ins can be added to the parent <b>RealTimeStylus</b>. The depth and breadth of the chain is limited to one child <b>RealTimeStylus</b> object. A child <b>RealTimeStylus</b> can have asynchronous plug-ins.

With the exception of <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusasyncplugincount">IRealTimeStylus::GetStylusAsyncPluginCount Method</a>, the asynchronous plug-in methods, such as <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addstylusasyncplugin">IRealTimeStylus::AddStylusAsyncPlugin Method</a>, return E_INVALIDOPERATION when called on a parent <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a>.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusasyncplugin">IRealTimeStylus::GetStylusAsyncPlugin Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removeallstylusasyncplugins">IRealTimeStylus::RemoveAllStylusAsyncPlugins Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removestylusasyncplugin">IRealTimeStylus::RemoveStylusAsyncPlugin Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>