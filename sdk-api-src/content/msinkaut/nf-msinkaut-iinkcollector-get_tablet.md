---
UID: NF:msinkaut.IInkCollector.get_Tablet
title: IInkCollector::get_Tablet
author: windows-sdk-content
description: Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input.
old-location: tablet\inkcollector_tablet.htm
old-project: tablet
ms.assetid: 170c3b43-6472-465b-bb09-22ba1a68c6e0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IInkCollector interface [Tablet PC],Tablet property, IInkCollector.Tablet, IInkCollector.get_Tablet, IInkCollector::Tablet, IInkCollector::get_Tablet, InkCollector.get_Tablet, Tablet property [Tablet PC], Tablet property [Tablet PC],IInkCollector interface, get_Tablet, msinkaut/IInkCollector::Tablet, msinkaut/IInkCollector::get_Tablet, tablet.inkcollector_tablet
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
 - IInkCollector.Tablet
 - IInkCollector.get_Tablet
 - InkCollector.get_Tablet
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::get_Tablet


## -description



Gets either the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.



This property is read-only.


## -parameters


## -remarks



For an object or control that collects ink, this property is valid only when the object or control is collecting ink from just one tablet. Accessing this property for an object or control that is collecting ink from all tablets generates an exception.

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.




## -see-also




<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/f107136f-3d75-4f2f-a89b-5e2f8e5a6c2e">Id Property</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode Method</a>
 

 

