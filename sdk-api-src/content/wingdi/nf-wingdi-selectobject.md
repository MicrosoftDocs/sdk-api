---
UID: NF:wingdi.SelectObject
title: SelectObject function
author: windows-sdk-content
description: The SelectObject function selects an object into the specified device context (DC). The new object replaces the previous object of the same type.
old-location: gdi\selectobject.htm
old-project: gdi
ms.assetid: a89b875e-923d-4048-bc61-8dea132cc56d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Bitmap, Brush, Font, Pen, Region, SelectObject, SelectObject function [Windows GDI], _win32_SelectObject, gdi.selectobject, wingdi/SelectObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - SelectObject
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SelectObject function


## -description


The <b>SelectObject</b> function selects an object into the specified device context (DC). The new object replaces the previous object of the same type.


## -parameters




### -param hdc [in]

A handle to the DC.


### -param h [in]

A handle to the object to be selected. The specified object must have been created by using one of the following functions.

<table>
<tr>
<th>Object</th>
<th>Functions</th>
</tr>
<tr>
<td width="40%"><a id="Bitmap"></a><a id="bitmap"></a><a id="BITMAP"></a><dl>
<dt><b>Bitmap</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>, <a href="https://msdn.microsoft.com/79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5">CreateBitmapIndirect</a>, <a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>, <a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>, <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>


Bitmaps can only be selected into memory DC's. A single bitmap cannot be selected into more than one DC at the same time.

</td>
</tr>
<tr>
<td width="40%"><a id="Brush"></a><a id="brush"></a><a id="BRUSH"></a><dl>
<dt><b>Brush</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a>, <a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>, <a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a>, <a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>, <a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>, <a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Font"></a><a id="font"></a><a id="FONT"></a><dl>
<dt><b>Font</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a>, <a href="https://msdn.microsoft.com/b7919fb6-8515-4f1b-af9c-dc7eac381b90">CreateFontIndirect</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Pen"></a><a id="pen"></a><a id="PEN"></a><dl>
<dt><b>Pen</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>, <a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Region"></a><a id="region"></a><a id="REGION"></a><dl>
<dt><b>Region</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ef9fc4f3-737e-4c10-a80b-8ae2097c17d1">CombineRgn</a>, <a href="https://msdn.microsoft.com/b4e9b210-8e22-42db-bb6e-65f1fb870eff">CreateEllipticRgn</a>, <a href="https://msdn.microsoft.com/bd30516e-1e05-4b7d-a6bf-7512cf3ef30f">CreateEllipticRgnIndirect</a>, <a href="https://msdn.microsoft.com/dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a">CreatePolygonRgn</a>, <a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>, <a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>


</td>
</tr>
</table>
 


## -returns



If the selected object is not a region and the function succeeds, the return value is a handle to the object being replaced. If the selected object is a region and the function succeeds, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region consists of a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region consists of more than one rectangle.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
</table>
 

If an error occurs and the selected object is not a region, the return value is <b>NULL</b>. Otherwise, it is HGDI_ERROR.




## -remarks



This function returns the previously selected object of the specified type. An application should always replace a new object with the original, default object after it has finished drawing with the new object.

An application cannot select a single bitmap into more than one DC at a time.

<b>ICM:</b> If the object being selected is a brush or a pen, color management is performed.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc">Setting the Pen or Brush Color</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ef9fc4f3-737e-4c10-a80b-8ae2097c17d1">CombineRgn</a>



<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>



<a href="https://msdn.microsoft.com/79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5">CreateBitmapIndirect</a>



<a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a>



<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/b4e9b210-8e22-42db-bb6e-65f1fb870eff">CreateEllipticRgn</a>



<a href="https://msdn.microsoft.com/bd30516e-1e05-4b7d-a6bf-7512cf3ef30f">CreateEllipticRgnIndirect</a>



<a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a>



<a href="https://msdn.microsoft.com/b7919fb6-8515-4f1b-af9c-dc7eac381b90">CreateFontIndirect</a>



<a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>



<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a>



<a href="https://msdn.microsoft.com/dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a">CreatePolygonRgn</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>
 

 

