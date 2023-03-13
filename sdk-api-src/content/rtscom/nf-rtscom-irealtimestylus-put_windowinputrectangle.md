---
UID: NF:rtscom.IRealTimeStylus.put_WindowInputRectangle
title: IRealTimeStylus::put_WindowInputRectangle (rtscom.h)
description: Gets or sets the window input rectangle for the RealTimeStylus Class object. (Put)
helpviewer_keywords: ["IRealTimeStylus interface [Tablet PC]","WindowInputRectangle property","IRealTimeStylus.WindowInputRectangle","IRealTimeStylus.get_WindowInputRectangle","IRealTimeStylus.put_WindowInputRectangle","IRealTimeStylus::WindowInputRectangle","IRealTimeStylus::get_WindowInputRectangle","IRealTimeStylus::put_WindowInputRectangle","WindowInputRectangle property [Tablet PC]","WindowInputRectangle property [Tablet PC]","IRealTimeStylus interface","e202be43-48c7-4fa4-b049-efdda3ef2ada","put_WindowInputRectangle","rtscom/IRealTimeStylus::WindowInputRectangle","rtscom/IRealTimeStylus::get_WindowInputRectangle","rtscom/IRealTimeStylus::put_WindowInputRectangle","tablet.irealtimestylus_windowinputrectangle"]
old-location: tablet\irealtimestylus_windowinputrectangle.htm
tech.root: tablet
ms.assetid: e202be43-48c7-4fa4-b049-efdda3ef2ada
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus interface [Tablet PC],WindowInputRectangle property, IRealTimeStylus.WindowInputRectangle, IRealTimeStylus.get_WindowInputRectangle, IRealTimeStylus.put_WindowInputRectangle, IRealTimeStylus::WindowInputRectangle, IRealTimeStylus::get_WindowInputRectangle, IRealTimeStylus::put_WindowInputRectangle, WindowInputRectangle property [Tablet PC], WindowInputRectangle property [Tablet PC],IRealTimeStylus interface, e202be43-48c7-4fa4-b049-efdda3ef2ada, put_WindowInputRectangle, rtscom/IRealTimeStylus::WindowInputRectangle, rtscom/IRealTimeStylus::get_WindowInputRectangle, rtscom/IRealTimeStylus::put_WindowInputRectangle, tablet.irealtimestylus_windowinputrectangle
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
 - IRealTimeStylus::put_WindowInputRectangle
 - rtscom/IRealTimeStylus::put_WindowInputRectangle
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
 - IRealTimeStylus.WindowInputRectangle
 - IRealTimeStylus.get_WindowInputRectangle
 - IRealTimeStylus.put_WindowInputRectangle
 - IRealTimeStylus.get_WindowInputRectangle
 - IRealTimeStylus.put_WindowInputRectangle
---

# IRealTimeStylus::put_WindowInputRectangle


## -description

Gets or sets the window input rectangle for the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.



This property is read/write.

## -parameters

## -remarks

Each <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object receives tablet pen data for specific section of a window based on the defined window input rectangle for that <b>RealTimeStylus Class</b> object.

The default value is an empty window input rectangle, <b>IRealTimeStylus::WindowInputRectangle Property</b>, value. When the <b>IRealTimeStylus::WindowInputRectangle Property</b> value is empty, {0, 0, 0, 0}, the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object collects pen input over the entire window, even after the window is resized.

After the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object starts collecting pen data, it continues to collect the data until the pen is raised, even if the pen is moved outside of the input region.

Use either an attached <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> object or the attached <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> object to uniquely handle pen data that is collected outside of the input region.

The E_INVALIDOPERATION HRESULT is returned when you attempt to set this property on a child <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
