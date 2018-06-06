---
UID: NF:msinkaut.IInkTablet.get_MaximumInputRectangle
title: IInkTablet::get_MaximumInputRectangle
author: windows-sdk-content
description: Gets the maximum input rectangle, in tablet device coordinates that the IInkTablet object supports.
old-location: tablet\iinktablet_maximuminputrectangle.htm
old-project: tablet
ms.assetid: 84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43, IInkTablet interface [Tablet PC],MaximumInputRectangle property, IInkTablet.MaximumInputRectangle, IInkTablet.get_MaximumInputRectangle, IInkTablet::MaximumInputRectangle, IInkTablet::get_MaximumInputRectangle, MaximumInputRectangle property [Tablet PC], MaximumInputRectangle property [Tablet PC],IInkTablet interface, get_MaximumInputRectangle, msinkaut/IInkTablet::MaximumInputRectangle, msinkaut/IInkTablet::get_MaximumInputRectangle, tablet.iinktablet_maximuminputrectangle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTablet.MaximumInputRectangle
 - IInkTablet.get_MaximumInputRectangle
 - IInkTablet.get_MaximumInputRectangle
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTablet::get_MaximumInputRectangle


## -description



Gets the maximum input rectangle, in tablet device coordinates that the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object supports.



This property is read-only.


## -parameters


## -remarks



The rectangle returned by the <b>MaximumInputRectangle</b> property specifies the maximum allowable space in which ink can be drawn.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>
 

 

