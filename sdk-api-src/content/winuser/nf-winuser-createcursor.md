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

# CreateCursor function


## -description


Creates a cursor having the specified size, bit patterns, and hot spot. 


## -parameters




### -param hInst [in, optional]

Type: <b>HINSTANCE</b>

A handle to the current instance of the application creating the cursor.


### -param xHotSpot [in]

Type: <b>int</b>

The horizontal position of the cursor's hot spot.


### -param yHotSpot [in]

Type: <b>int</b>

The vertical position of the cursor's hot spot.


### -param nWidth [in]

Type: <b>int</b>

The width of the cursor, in pixels.


### -param nHeight [in]

Type: <b>int</b>

The height of the cursor, in pixels.


### -param pvANDPlane [in]

Type: <b>const VOID*</b>

An array of bytes that contains the bit values for the 
					AND mask of the cursor, as in a device-dependent monochrome bitmap. 


### -param pvXORPlane [in]

Type: <b>const VOID*</b>

An array of bytes that contains the bit values for the 
					XOR mask of the cursor, as in a device-dependent monochrome bitmap. 


## -returns



Type: <b>HCURSOR</b>

If the function succeeds, the return value is a handle to the cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <i>nWidth</i> and <i>nHeight</i> parameters must specify a width and height that are supported by the current display driver, because the system cannot create cursors of other sizes. To determine the width and height supported by the display driver, use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function, specifying the <b>SM_CXCURSOR</b> or <b>SM_CYCURSOR</b> value. 

Before closing, an application must call the <a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a> function to free any system resources associated with the cursor. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is in terms of physical coordinates, and  is not affected by the DPI of the calling thread. Note that the cursor created may still be scaled to match the DPI of any given window it is drawn into.


#### Examples

For an example, see <a href="using_cursors.htm">Creating a Cursor</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>



<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>
 

 

