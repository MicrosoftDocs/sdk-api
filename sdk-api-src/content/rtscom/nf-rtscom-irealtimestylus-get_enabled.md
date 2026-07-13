---
UID: NF:rtscom.IRealTimeStylus.get_Enabled
title: IRealTimeStylus::get_Enabled (rtscom.h)
description: Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data. (Get)
helpviewer_keywords: ["Enabled property [Tablet PC]","Enabled property [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","Enabled property","IRealTimeStylus.Enabled","IRealTimeStylus.get_Enabled","IRealTimeStylus.put_Enabled","IRealTimeStylus::Enabled","IRealTimeStylus::get_Enabled","IRealTimeStylus::put_Enabled","e96e27d7-b453-49a7-b684-b3dd5f94c378","get_Enabled","rtscom/IRealTimeStylus::Enabled","rtscom/IRealTimeStylus::get_Enabled","rtscom/IRealTimeStylus::put_Enabled","tablet.irealtimestylus_enabled"]
old-location: tablet\irealtimestylus_enabled.htm
tech.root: tablet
ms.assetid: e96e27d7-b453-49a7-b684-b3dd5f94c378
ms.date: 12/05/2018
ms.keywords: Enabled property [Tablet PC], Enabled property [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],Enabled property, IRealTimeStylus.Enabled, IRealTimeStylus.get_Enabled, IRealTimeStylus.put_Enabled, IRealTimeStylus::Enabled, IRealTimeStylus::get_Enabled, IRealTimeStylus::put_Enabled, e96e27d7-b453-49a7-b684-b3dd5f94c378, get_Enabled, rtscom/IRealTimeStylus::Enabled, rtscom/IRealTimeStylus::get_Enabled, rtscom/IRealTimeStylus::put_Enabled, tablet.irealtimestylus_enabled
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
 - IRealTimeStylus::get_Enabled
 - rtscom/IRealTimeStylus::get_Enabled
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
 - IRealTimeStylus.Enabled
 - IRealTimeStylus.get_Enabled
 - IRealTimeStylus.put_Enabled
 - IRealTimeStylus.get_Enabled
 - IRealTimeStylus.put_Enabled
---

# IRealTimeStylus::get_Enabled


## -description

Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object collects tablet pen data.



This property is read/write.

## -parameters

## -remarks

Multiple <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> objects can exist on the same window provided they are not enabled with overlapping window input rectangles. Enabled <b>RealTimeStylus</b> objects on the same window with overlapping input rectangles result in undetermined behavior.

<div class="alert"><b>Note</b>  An overlap can occur without an error if only one of the input rectangles is enabled at any one time.</div>
<div> </div>
A child <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object must be connected to be enabled.

Although a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object can be enabled when it has no plug-ins attached to it, it must have at least one plug-in to be useful.

You receive no events when an object is not enabled.

When the <b>IRealTimeStylus::Enabled Property</b> of a container control is set to <b>false</b>, all of its contained controls are also disabled.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue">IRealTimeStylus::AddCustomStylusDataToQueue Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstyluses">IRealTimeStylus::GetStyluses Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet">IRealTimeStylus::GetTabletContextIdFromTablet Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid">IRealTimeStylus::GetTabletFromTabletContextId Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
