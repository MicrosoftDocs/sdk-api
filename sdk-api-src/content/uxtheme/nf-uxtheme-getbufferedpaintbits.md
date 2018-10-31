---
UID: NF:uxtheme.GetBufferedPaintBits
title: GetBufferedPaintBits function
author: windows-sdk-content
description: Retrieves a pointer to the buffer bitmap if the buffer is a device-independent bitmap (DIB).
old-location: controls\GetBufferedPaintBits.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpaintbits.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetBufferedPaintBits, GetBufferedPaintBits function [Windows Controls], _shell_GetBufferedPaintBits, _shell_GetBufferedPaintBits_cpp, controls.GetBufferedPaintBits, controls._shell_GetBufferedPaintBits, uxtheme/GetBufferedPaintBits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - GetBufferedPaintBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetBufferedPaintBits function


## -description


Retrieves a pointer to the buffer bitmap if the buffer is a device-independent bitmap (DIB).


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="https://msdn.microsoft.com/en-us/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a>.


### -param ppbBuffer [out]

Type: <b><a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a>**</b>

When this function returns, contains a pointer to the address of the buffer bitmap pixels.


### -param pcxRow [out]

Type: <b>int*</b>

When this function returns, contains a pointer to the width, in pixels, of the buffer bitmap. This value is not necessarily equal to the buffer width. It may be larger.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful, or an error value otherwise. If an error occurs, <i>ppbBuffer</i>  is set to <b>NULL</b> and <i>pcxRow</i> is set to zero.




## -remarks



The number of bits per pixel depends on the pixel format passed to <a href="https://msdn.microsoft.com/en-us/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb759835(v=VS.85).aspx">BP_BUFFERFORMAT</a>



<a href="https://msdn.microsoft.com/56b39a3d-48a4-4620-9652-ec41ea4d6423">Device-Independent Bitmaps</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

