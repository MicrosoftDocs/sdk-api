---
UID: NF:msinkaut.IInkCursor.get_Id
title: IInkCursor::get_Id
author: windows-sdk-content
description: Gets the identifier of an object.
old-location: tablet\iinkcursor_id.htm
old-project: tablet
ms.assetid: e302ef9f-da38-4190-af78-d26f9fc86543
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ID property [Tablet PC], ID property [Tablet PC],IInkCursor interface, IInkCursor interface [Tablet PC],ID property, IInkCursor.ID, IInkCursor.get_ID, IInkCursor.get_Id, IInkCursor::ID, IInkCursor::get_ID, IInkCursor::get_Id, get_Id, msinkaut/IInkCursor::ID, msinkaut/IInkCursor::get_ID, tablet.iinkcursor_id
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
 - IInkCursor.ID
 - IInkCursor.get_ID
 - IInkCursor.get_ID
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCursor::get_Id


## -description



Gets the identifier of an object.



This property is read-only.


## -parameters


## -remarks



An object's identifier never changes.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to <b>SC_HOTKEY</b> or <b>SC_TASKLIST</b>; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">InkCursor Interface</a>
 

 

