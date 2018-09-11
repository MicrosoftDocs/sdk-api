---
UID: NF:vfw.DrawDibGetBuffer
title: DrawDibGetBuffer function
author: windows-sdk-content
description: The DrawDibGetBuffer function retrieves the location of the buffer used by DrawDib for decompression.
old-location: multimedia\drawdibgetbuffer.htm
tech.root: Multimedia
ms.assetid: 6b3e1d3a-2227-4a27-91aa-8767a3d76bc4
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: DrawDibGetBuffer, DrawDibGetBuffer function [Windows Multimedia], _win32_DrawDibGetBuffer, multimedia.drawdibgetbuffer, vfw/DrawDibGetBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibGetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawDibGetBuffer function


## -description



The <b>DrawDibGetBuffer</b> function retrieves the location of the buffer used by DrawDib for decompression.




## -parameters




### -param hdd

Handle to a DrawDib DC.
          


### -param lpbi

Pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=16913">BITMAPINFO</a> structure. This structure is made up of a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure and a 256-entry table defining the colors used by the bitmap.
          


### -param dwSize

Size, in bytes, of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure pointed to by <i>lpbi</i>


### -param dwFlags

Reserved; must be zero.
          


## -returns



Returns the address of the buffer or <b>NULL</b> if no buffer is used. if <i>lpbr</i> is not <b>NULL</b>, it is filled with a copy of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure describing the buffer.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

