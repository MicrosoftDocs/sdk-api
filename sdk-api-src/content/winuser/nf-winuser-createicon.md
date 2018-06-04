---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CreateIcon function


## -description


Creates an icon that has the specified size, colors, and bit patterns.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the module creating the icon.


### -param nWidth [in]

Type: <b>int</b>

The width, in pixels, of the icon.


### -param nHeight [in]

Type: <b>int</b>

The height, in pixels, of the icon.


### -param cPlanes [in]

Type: <b>BYTE</b>

The number of planes in the XOR bitmask of the icon.


### -param cBitsPixel [in]

Type: <b>BYTE</b>

The number of bits-per-pixel in the XOR bitmask of the icon.


### -param lpbANDbits [in]

Type: <b>const BYTE*</b>

An array of bytes that contains the bit values for the AND bitmask of the icon. This bitmask describes a monochrome bitmap.


### -param lpbXORbits [in]

Type: <b>const BYTE*</b>

An array of bytes that contains the bit values for the XOR bitmask of the icon. This bitmask describes a monochrome or device-dependent color bitmap. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to an icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <i>nWidth</i> and <i>nHeight</i> parameters must specify a width and height supported by the current display driver, because the system cannot create icons of other sizes. To determine the width and height supported by the display driver, use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function, specifying the <b>SM_CXICON</b> or <b>SM_CYICON</b> value. 

<b>CreateIcon</b> applies the following truth table to the AND and XOR bitmasks.

<table class="clsStd">
<tr>
<th>AND bitmask</th>
<th>XOR bitmask</th>
<th>Display</th>
</tr>
<tr>
<td>0</td>
<td>0</td>
<td>Black </td>
</tr>
<tr>
<td>0</td>
<td>1</td>
<td>White </td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>Screen </td>
</tr>
<tr>
<td>1</td>
<td>1</td>
<td>Reverse screen </td>
</tr>
</table>
 

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.


#### Examples

For an example, see <a href="using_icons.htm">Creating an Icon</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Other Resources</b>
 

 

