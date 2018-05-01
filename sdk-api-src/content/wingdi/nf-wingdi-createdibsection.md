---
UID: NF:wingdi.CreateDIBSection
title: CreateDIBSection function
author: windows-driver-content
description: The CreateDIBSection function creates a DIB that applications can write to directly.
old-location: gdi\createdibsection.htm
old-project: gdi
ms.assetid: 9276ec84-2860-42be-a9f8-d4efb8d25eec
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CreateDIBSection, CreateDIBSection function [Windows GDI], DIB_PAL_COLORS, DIB_RGB_COLORS, _win32_CreateDIBSection, gdi.createdibsection, wingdi/CreateDIBSection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-l1-1-0.dll
-	Ext-MS-Win-GDI-Draw-l1-1-1.dll
-	ext-ms-win-gdi-draw-l1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	CreateDIBSection
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateDIBSection function


## -description


The <b>CreateDIBSection</b> function creates a DIB that applications can write to directly. The function gives you a pointer to the location of the bitmap bit values. You can supply a handle to a file-mapping object that the function will use to create the bitmap, or you can let the system allocate the memory for the bitmap.


## -parameters




### -param hdc [in]

A handle to a device context. If the value of <i>iUsage</i> is DIB_PAL_COLORS, the function uses this device context's logical palette to initialize the DIB colors.


### -param pbmi [in]

A pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure that specifies various attributes of the DIB, including the bitmap dimensions and colors.


### -param usage

TBD


### -param ppvBits [out]

A pointer to a variable that receives a pointer to the location of the DIB bit values.


### -param hSection [in]

A handle to a file-mapping object that the function will use to create the DIB. This parameter can be <b>NULL</b>.

If <i>hSection</i> is not <b>NULL</b>, it must be a handle to a file-mapping object created by calling the <a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a> function with the PAGE_READWRITE or PAGE_WRITECOPY flag. Read-only DIB sections are not supported. Handles created by other means will cause <b>CreateDIBSection</b> to fail.

If <i>hSection</i> is not <b>NULL</b>, the <b>CreateDIBSection</b> function locates the bitmap bit values at offset <i>dwOffset</i> in the file-mapping object referred to by <i>hSection</i>. An application can later retrieve the <i>hSection</i> handle by calling the <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> function with the <b>HBITMAP</b> returned by <b>CreateDIBSection</b>.

If <i>hSection</i> is <b>NULL</b>, the system allocates memory for the DIB. In this case, the <b>CreateDIBSection</b> function ignores the <i>dwOffset</i> parameter. An application cannot later obtain a handle to this memory. The <b>dshSection</b> member of the <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a> structure filled in by calling the <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> function will be <b>NULL</b>.


### -param offset

TBD




#### - dwOffset [in]

The offset from the beginning of the file-mapping object referenced by <i>hSection</i> where storage for the bitmap bit values is to begin. This value is ignored if <i>hSection</i> is <b>NULL</b>. The bitmap bit values are aligned on doubleword boundaries, so <i>dwOffset</i> must be a multiple of the size of a <b>DWORD</b>.


#### - iUsage [in]

The type of data contained in the <b>bmiColors</b> array member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure pointed to by <i>pbmi</i> (either logical palette indexes or literal RGB values). The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIB_PAL_COLORS"></a><a id="dib_pal_colors"></a><dl>
<dt><b>DIB_PAL_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The <b>bmiColors</b> member is an array of 16-bit indexes into the logical palette of the device context specified by <i>hdc</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure contains an array of literal RGB values.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a handle to the newly created DIB, and *<i>ppvBits</i> points to the bitmap bit values.

If the function fails, the return value is <b>NULL</b>, and *<i>ppvBits</i> is <b>NULL</b>.

This function can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>
 




## -remarks



As noted above, if <i>hSection</i> is <b>NULL</b>, the system allocates memory for the DIB. The system closes the handle to that memory when you later delete the DIB by calling the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function. If <i>hSection</i> is not <b>NULL</b>, you must close the <i>hSection</i> memory handle yourself after calling <b>DeleteObject</b> to delete the bitmap.

You cannot paste a DIB section from one application into another application.

<b>CreateDIBSection</b> does not use the <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> parameters <i>biXPelsPerMeter</i> or <i>biYPelsPerMeter</i> and will not provide resolution information in the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


         You need to guarantee that the GDI subsystem has completed any drawing to a bitmap created by <b>CreateDIBSection</b> before you draw to the bitmap yourself. Access to the bitmap must be synchronized. Do this by calling the <a href="https://msdn.microsoft.com/6d2f398d-7a30-4b14-81de-23ab10e1749c">GdiFlush</a> function. This applies to any use of the pointer to the bitmap bit values, including passing the pointer in calls to functions such as <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>.

<b>ICM:</b> No color management is done.




## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="http://msdn.microsoft.com/en-us/library/aa366537(VS.85).aspx">CreateFileMapping</a>



<a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/6d2f398d-7a30-4b14-81de-23ab10e1749c">GdiFlush</a>



<a href="https://msdn.microsoft.com/3e3319be-8a3d-4ac2-ba36-9dbf18243472">GetDIBColorTable</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/f301c34d-6e8e-4dc8-b3f3-0fdc658d09e3">SetDIBColorTable</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>
 

 

