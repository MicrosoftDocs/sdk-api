---
UID: NF:msinkaut.IInkOverlay.get_Tablet
title: IInkOverlay::get_Tablet
author: windows-sdk-content
description: Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input.
old-location: tablet\inkoverlay_tablet.htm
tech.root: tablet
ms.assetid: 88da4f91-2baf-4152-adc2-a6f91bc2c9e3
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IInkOverlay interface [Tablet PC],Tablet property, IInkOverlay.Tablet, IInkOverlay.get_Tablet, IInkOverlay::Tablet, IInkOverlay::get_Tablet, InkOverlay.get_Tablet, Tablet property [Tablet PC], Tablet property [Tablet PC],IInkOverlay interface, get_Tablet, msinkaut/IInkOverlay::Tablet, msinkaut/IInkOverlay::get_Tablet, put_Tablet, tablet.inkoverlay_tablet
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.Tablet
 - IInkOverlay.get_Tablet
 - InkOverlay.get_Tablet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::get_Tablet


## -description



Gets either the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.



This property is read-only.


## -parameters


## -remarks



For an object or control that collects ink, this property is valid only when the object or control is collecting ink from just one tablet. Accessing this property for an object or control that is collecting ink from all tablets generates an exception.

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.




## -see-also




<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/f107136f-3d75-4f2f-a89b-5e2f8e5a6c2e">Id Property</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode Method</a>
 

 

