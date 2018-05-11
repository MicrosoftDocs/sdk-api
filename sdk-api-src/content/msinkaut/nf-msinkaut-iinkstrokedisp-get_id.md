---
UID: NF:msinkaut.IInkStrokeDisp.get_ID
title: IInkStrokeDisp::get_ID
author: windows-driver-content
description: Gets the identifier of an object.
old-location: tablet\iinkstrokedisp_id.htm
old-project: tablet
ms.assetid: f8e9d2b2-c3d1-4ea8-aed6-649bf6d4d353
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ID property [Tablet PC], ID property [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],ID property, IInkStrokeDisp.ID, IInkStrokeDisp.get_ID, IInkStrokeDisp.get_Id, IInkStrokeDisp::ID, IInkStrokeDisp::get_ID, get_ID, msinkaut/IInkStrokeDisp::ID, msinkaut/IInkStrokeDisp::get_ID, tablet.iinkstrokedisp_id
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.ID
-	IInkStrokeDisp.get_ID
-	IInkStrokeDisp.get_Id
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::get_ID


## -description



Gets the identifier of an object.



This property is read-only.


## -parameters


## -remarks



An object's identifier never changes.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to <b>SC_HOTKEY</b> or <b>SC_TASKLIST</b>; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

