---
UID: NF:commctrl.CreateMappedBitmap
title: CreateMappedBitmap function
author: windows-driver-content
description: Creates a bitmap for use in a toolbar.
old-location: controls\CreateMappedBitmap.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\toolbar\functions\createmappedbitmap.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: CMB_MASKED, CreateMappedBitmap, CreateMappedBitmap function [Windows Controls], _win32_CreateMappedBitmap, _win32_CreateMappedBitmap_cpp, commctrl/CreateMappedBitmap, controls.CreateMappedBitmap, controls._win32_CreateMappedBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
-	Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
-	CreateMappedBitmap
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# CreateMappedBitmap function


## -description


Creates a bitmap for use in a toolbar. 


## -parameters




### -param hInstance

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Handle to the module instance with the executable file that contains the bitmap resource. 


### -param idBitmap

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT_PTR</a></b>

Resource identifier of the bitmap resource. 


### -param wFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bitmap flag. This parameter can be zero or the following value: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMB_MASKED"></a><a id="cmb_masked"></a><dl>
<dt><b>CMB_MASKED</b></dt>
</dl>
</td>
<td width="60%">
Uses a bitmap as a mask.

</td>
</tr>
</table>
 


### -param lpColorMap [in]

Type: <b>LPCOLORMAP</b>

Pointer to a <a href="https://msdn.microsoft.com/50838fd1-1886-4c6d-ad09-9646036ae9cf">COLORMAP</a> structure that contains the color information needed to map the bitmaps. If this parameter is <b>NULL</b>, the function uses the default color map. 


### -param iNumMaps

Type: <b>int</b>

Number of color maps pointed to by 
					<i>lpColorMap</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

Returns the handle to the bitmap if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function creates a new bitmap using the bitmap data and colors specified by the bitmap resource and the color mapping information. 

This function is fully supported only for images with color maps; that is, images with 256 or fewer colors.


#### Examples

The following example code creates a bitmap from a resource and makes the color black appear transparent by mapping it to the system color for a button face.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &amp;colorMap, 1);</pre>
</td>
</tr>
</table></span></div>


