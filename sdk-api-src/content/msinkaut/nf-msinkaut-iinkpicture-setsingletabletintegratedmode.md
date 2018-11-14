---
UID: NF:msinkaut.IInkPicture.SetSingleTabletIntegratedMode
title: IInkPicture::SetSingleTabletIntegratedMode
author: windows-sdk-content
description: Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.
old-location: tablet\inkpicture_setsingletabletintegratedmode.htm
tech.root: tablet
ms.assetid: b611a078-b38e-4f9b-834f-9a2aa9684931
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 96787996-c0fd-455f-952e-90ddc8640253, IInkPicture interface [Tablet PC],SetSingleTabletIntegratedMode method, IInkPicture.SetSingleTabletIntegratedMode, IInkPicture::SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode method [Tablet PC], SetSingleTabletIntegratedMode method [Tablet PC],IInkPicture interface, msinkaut/IInkPicture::SetSingleTabletIntegratedMode, tablet.inkpicture_setsingletabletintegratedmode
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
 - IInkPicture.SetSingleTabletIntegratedMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkPicture.SetSingleTabletIntegratedMode
: 
---

# IInkPicture::SetSingleTabletIntegratedMode


## -description



Allows the ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.




## -parameters




### -param Tablet [in]

The tablet on which ink is collected, or drawn.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_COLLECTOR_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
Cannot change modes while the collector is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
<i>tablet</i> does not point to a compatible Ink object.

</td>
</tr>
</table>
 




## -remarks



To allow the ink collector to collect ink from all tablets, call the <a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode</a> method.

<div class="alert"><b>Note</b>  The ink collector object or control that collects ink must be disabled before calling this method. To disable the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, set the <a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled</a> property to <b>FALSE</b>. To disable the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control, set the <a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled</a> property to <b>FALSE</b>. After calling the <b>SetSingleTabletIntegratedMode</b> method, re-enable the object or control by setting the <a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled</a> (or <b>InkEnabled</b>) property to <b>TRUE</b>.</div>
<div> </div>
When this method is called, the <a href="https://msdn.microsoft.com/815f4895-d418-4336-9420-2405bcd5cfb3">Cursors</a> property of the ink collector is set to the empty collection.




## -see-also




<a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled Property</a>



<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>



<a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode Method</a>
 

 

