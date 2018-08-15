---
UID: NF:msinkaut.IInkCursor.get_Tablet
title: IInkCursor::get_Tablet
author: windows-sdk-content
description: Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input.
old-location: tablet\inkcursor_tablet.htm
old-project: tablet
ms.assetid: 85bbf314-e1fe-43fb-b743-d648aa6a54cd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 85bbf314-e1fe-43fb-b743-d648aa6a54cd, IInkCursor interface [Tablet PC],Tablet property, IInkCursor.Tablet, IInkCursor.get_Tablet, IInkCursor::Tablet, IInkCursor::get_Tablet, Tablet property [Tablet PC], Tablet property [Tablet PC],IInkCursor interface, get_Tablet, msinkaut/IInkCursor::Tablet, msinkaut/IInkCursor::get_Tablet, tablet.inkcursor_tablet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
 - IInkCursor.Tablet
 - IInkCursor.get_Tablet
 - IInkCursor.get_Tablet
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCursor::get_Tablet


## -description



Gets either the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.



This property is read-only.


## -parameters


## -remarks



For an object or control that collects ink, this property is valid only when the object or control is collecting ink from just one tablet. Accessing this property for an object or control that is collecting ink from all tablets generates an exception.

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.




## -see-also




<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/f107136f-3d75-4f2f-a89b-5e2f8e5a6c2e">Id Property</a>



<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">InkCursor Interface</a>



<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode Method</a>
 

 

