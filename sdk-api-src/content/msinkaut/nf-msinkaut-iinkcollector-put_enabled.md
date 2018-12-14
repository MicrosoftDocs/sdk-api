---
UID: NF:msinkaut.IInkCollector.put_Enabled
title: IInkCollector::put_Enabled
author: windows-sdk-content
description: Gets or sets a value that specifies whether the InkCollector object collects pen input (in-air packets, cursor in range events, and so on).
old-location: tablet\inkcollector_enabled.htm
tech.root: tablet
ms.assetid: ab55a399-1990-4cfc-a4ab-834a5db8d7a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Enabled property [Tablet PC], Enabled property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],Enabled property, IInkCollector.Enabled, IInkCollector.put_Enabled, IInkCollector::Enabled, IInkCollector::get_Enabled, IInkCollector::put_Enabled, InkCollector.get_Enabled, InkCollector.put_Enabled, ab55a399-1990-4cfc-a4ab-834a5db8d7a9, get_Enabled, msinkaut/IInkCollector::Enabled, msinkaut/IInkCollector::get_Enabled, msinkaut/IInkCollector::put_Enabled, put_Enabled, tablet.inkcollector_enabled
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
 - IInkCollector.Enabled
 - IInkCollector.get_Enabled
 - IInkCollector.put_Enabled
 - put_Enabled
 - IInkCollector.put_Enabled
 - InkCollector.get_Enabled
 - InkCollector.put_Enabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCollector::put_Enabled


## -description



Gets or sets  a value that specifies whether the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object collects pen input (in-air packets, cursor in range events, and so on).



This property is read/write.


## -parameters


## -remarks



If an enabled object's window input rectangle (set in the constructor or with the <a href="https://msdn.microsoft.com/b46139db-0473-4cd3-8f1b-d303f3430470">SetWindowInputRectangle</a> method) of an enabled object overlaps the window input rectangle of another enabled object, the E_INK_OVERLAPPING_INPUT_RECT error is returned. Overlap can occur without an error as long as only one of the input rectangles is enabled at any known time.

While an object is not enabled, you receive no events.

When a container control has its <b>Enabled</b> property set to <b>FALSE</b>, all of its contained controls are disabled as well.

You cannot set the <b>Enabled</b> property to <b>FALSE</b> while the object is collecting ink (<a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a> property is <b>TRUE</b>).

We recommend that you set <b>Enabled</b> set to <b>FALSE</b> when the application shuts down.

<div class="alert"><b>Note</b>  Setting this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>
This property must be set to <b>FALSE</b> before setting or calling specific properties and methods of the object. If you try to change the specified properties or methods, an error occurs. The following properties and methods cannot be set or called unless the <b>Enabled</b> property is first set to <b>FALSE</b>:

Properties

<ul>
<li>
<a href="https://msdn.microsoft.com/638da0e4-10cc-47e7-91ad-807be3ff8c2d">AttachMode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a>
</li>
<li>
<a href="https://msdn.microsoft.com/62881a0e-3932-49a1-8e7d-3e74474f2214">Ink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d128fb84-f3cb-4e10-8764-ccb060841383">MarginX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6cba076e-6392-4f0a-a80d-3df903d0ba13">MarginY</a>
</li>
</ul>
Methods

<ul>
<li>
<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/638da0e4-10cc-47e7-91ad-807be3ff8c2d">AttachMode Property</a>



<a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk Property</a>



<a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode Property [InkCollector Class]</a>



<a href="https://msdn.microsoft.com/3b734da3-5784-4504-b22e-b86844d42f4e">EditingMode Property [InkOverlay Class]</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://msdn.microsoft.com/62881a0e-3932-49a1-8e7d-3e74474f2214">Ink Property [InkCollector/InkOverLay Class]</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/d128fb84-f3cb-4e10-8764-ccb060841383">MarginX Property</a>



<a href="https://msdn.microsoft.com/6cba076e-6392-4f0a-a80d-3df903d0ba13">MarginY Property</a>



<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode Method</a>



<a href="https://msdn.microsoft.com/b46139db-0473-4cd3-8f1b-d303f3430470">SetWindowInputRectangle Method</a>



<a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd Property</a>
 

 

