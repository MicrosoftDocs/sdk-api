---
UID: NF:winuser.LoadBitmapA
title: LoadBitmapA function
author: windows-sdk-content
description: The LoadBitmap function loads the specified bitmap resource from a module's executable file.
old-location: gdi\loadbitmap.htm
old-project: gdi
ms.assetid: 5eed5f78-deaf-4b23-986e-4802dc05936c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LoadBitmap, LoadBitmap function [Windows GDI], LoadBitmapA, LoadBitmapW, _win32_LoadBitmap, gdi.loadbitmap, winuser/LoadBitmap, winuser/LoadBitmapA, winuser/LoadBitmapW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadBitmapW (Unicode) and LoadBitmapA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - LoadBitmap
 - LoadBitmapA
 - LoadBitmapW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadBitmapA function


## -description


<p class="CCE_Message">[<b>LoadBitmap</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="_win32_loadimage_cpp">LoadImage</a> and <a href="https://msdn.microsoft.com/3102007e-e9f7-46d8-ae10-cf156d2131f6">DrawFrameControl</a>.]

The <b>LoadBitmap</b> function loads the specified bitmap resource from a module's executable file.


## -parameters




### -param hInstance [in]

A handle to the instance of the module whose executable file contains the bitmap to be loaded.


### -param lpBitmapName [in]

A pointer to a null-terminated string that contains the name of the bitmap resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. The <a href="_win32_makeintresource_cpp">MAKEINTRESOURCE</a> macro can be used to create this value.


## -returns



If the function succeeds, the return value is the handle to the specified bitmap.

If the function fails, the return value is <b>NULL</b>.




## -remarks



If the bitmap pointed to by the <i>lpBitmapName</i> parameter does not exist or there is insufficient memory to load the bitmap, the function fails.

<b>LoadBitmap</b> creates a compatible bitmap of the display, which cannot be selected to a printer. To load a bitmap that you can select to a printer, call <a href="_win32_loadimage_cpp">LoadImage</a> and specify LR_CREATEDIBSECTION to create a DIB section. A DIB section can be selected to any device.

An application can use the <b>LoadBitmap</b> function to access predefined bitmaps. To do so, the application must set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpBitmapName</i> parameter to one of the following values.

<table>
<tr>
<th>Bitmap name</th>
<th>Bitmap name</th>
</tr>
<tr>
<td>OBM_BTNCORNERS</td>
<td>OBM_OLD_RESTORE</td>
</tr>
<tr>
<td>OBM_BTSIZE</td>
<td>OBM_OLD_RGARROW</td>
</tr>
<tr>
<td>OBM_CHECK</td>
<td>OBM_OLD_UPARROW</td>
</tr>
<tr>
<td>OBM_CHECKBOXES</td>
<td>OBM_OLD_ZOOM</td>
</tr>
<tr>
<td>OBM_CLOSE</td>
<td>OBM_REDUCE</td>
</tr>
<tr>
<td>OBM_COMBO</td>
<td>OBM_REDUCED</td>
</tr>
<tr>
<td>OBM_DNARROW</td>
<td>OBM_RESTORE</td>
</tr>
<tr>
<td>OBM_DNARROWD</td>
<td>OBM_RESTORED</td>
</tr>
<tr>
<td>OBM_DNARROWI</td>
<td>OBM_RGARROW</td>
</tr>
<tr>
<td>OBM_LFARROW</td>
<td>OBM_RGARROWD</td>
</tr>
<tr>
<td>OBM_LFARROWD</td>
<td>OBM_RGARROWI</td>
</tr>
<tr>
<td>OBM_LFARROWI</td>
<td>OBM_SIZE</td>
</tr>
<tr>
<td>OBM_MNARROW</td>
<td>OBM_UPARROW</td>
</tr>
<tr>
<td>OBM_OLD_CLOSE</td>
<td>OBM_UPARROWD</td>
</tr>
<tr>
<td>OBM_OLD_DNARROW</td>
<td>OBM_UPARROWI</td>
</tr>
<tr>
<td>OBM_OLD_LFARROW</td>
<td>OBM_ZOOM</td>
</tr>
<tr>
<td>OBM_OLD_REDUCE</td>
<td>OBM_ZOOMD</td>
</tr>
</table>
 

Bitmap names that begin with OBM_OLD represent bitmaps used by 16-bit versions of Windows earlier than 3.0.

For an application to use any of the OBM_ constants, the constant OEMRESOURCE must be defined before the Windows.h header file is included.

The application must call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete each bitmap handle returned by the <b>LoadBitmap</b> function.


#### Examples

For an example, see Example of Menu-Item Bitmaps in <a href="_win32_Using_Menus_cpp">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/3102007e-e9f7-46d8-ae10-cf156d2131f6">DrawFrameControl</a>



<a href="_win32_loadcursor_cpp">LoadCursor</a>



<a href="_win32_loadicon_cpp">LoadIcon</a>



<a href="_win32_loadimage_cpp">LoadImage</a>



<a href="_win32_makeintresource_cpp">MAKEINTRESOURCE</a>
 

 

