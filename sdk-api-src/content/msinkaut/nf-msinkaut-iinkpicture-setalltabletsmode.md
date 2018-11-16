---
UID: NF:msinkaut.IInkPicture.SetAllTabletsMode
title: IInkPicture::SetAllTabletsMode
author: windows-sdk-content
description: Allows an ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from any tablet attached to the Tablet PC.
old-location: tablet\inkpicture_setalltabletsmode.htm
tech.root: tablet
ms.assetid: 30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IInkPicture interface [Tablet PC],SetAllTabletsMode method, IInkPicture.SetAllTabletsMode, IInkPicture::SetAllTabletsMode, SetAllTabletsMode, SetAllTabletsMode method [Tablet PC], SetAllTabletsMode method [Tablet PC],IInkPicture interface, cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8, msinkaut/IInkPicture::SetAllTabletsMode, tablet.inkpicture_setalltabletsmode
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
 - IInkPicture.SetAllTabletsMode
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
- IInkPicture.SetAllTabletsMode
: 
---

# IInkPicture::SetAllTabletsMode


## -description



Allows an ink collector  (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.




## -parameters




### -param UseMouseForInput [in, optional]

Optional. <b>VARIANT_TRUE</b> to use the mouse as an input device; otherwise, <b>VARIANT_FALSE. </b>The default value is <b>VARIANT_TRUE</b>.


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
<dt><b>E_INK_COLLECTOR_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
Cannot change modes while the InkCollector is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
</table>
 




## -remarks



This is the default mode for an object or control that collects ink. To allow the ink collector to collect ink from only one tablet, call the <a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode</a> method.

<div class="alert"><b>Note</b>  The ink collector must be disabled before calling this method. To disable the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, set the <a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled</a> property to <b>FALSE</b>. To disable the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control, set the <a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled</a> property to <b>FALSE</b>. After calling the <b>SetAllTabletsMode</b> method, re-enable the object or control by setting the <b>Enabled</b> (or <b>InkEnabled</b>) property to <b>VARIANT_TRUE</b>.</div>
<div> </div>
When an ink collector switches from ink collection using a single tablet to ink collection using all tablets, the <a href="https://msdn.microsoft.com/815f4895-d418-4336-9420-2405bcd5cfb3">Cursors</a> property is set to the empty collection.

<div class="alert"><b>Note</b>  If the <b>SetAllTabletsMode</b> method is called with the <i>useMouse</i> parameter set to <b>VARIANT_TRUE</b>, the mouse is used as an input device. If the <b>SetAllTabletsMode</b> method is then called with the <i>useMouse</i> parameter set to <b>VARIANT_FALSE</b>, the mouse is not removed from the <a href="https://msdn.microsoft.com/815f4895-d418-4336-9420-2405bcd5cfb3">Cursors</a> property.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled Property</a>



<a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors Interface</a>



<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode Method</a>
 

 

