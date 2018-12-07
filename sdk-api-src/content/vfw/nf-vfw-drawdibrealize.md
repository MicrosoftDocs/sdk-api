---
UID: NF:vfw.DrawDibRealize
title: DrawDibRealize function
author: windows-sdk-content
description: The DrawDibRealize function realizes the palette of the DrawDib DC for use with the specified DC.
old-location: multimedia\drawdibrealize.htm
tech.root: Multimedia
ms.assetid: 4723c8a4-36af-4543-b6df-d51f68a3e94d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawDibRealize, DrawDibRealize function [Windows Multimedia], _win32_DrawDibRealize, multimedia.drawdibrealize, vfw/DrawDibRealize
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
 - DrawDibRealize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawDibRealize function


## -description



The <b>DrawDibRealize</b> function realizes the palette of the DrawDib DC for use with the specified DC.




## -parameters




### -param hdd

Handle to a DrawDib DC.


### -param hdc

Handle to the DC containing the palette.


### -param fBackground

Background palette flag. If this value is nonzero, the palette is a background palette. If this value is zero and the DC is attached to a window, the logical palette becomes the foreground palette when the window has the input focus. (A DC is attached to a window when the window class style is CS_OWNDC or when the DC is obtained by using the <a href="http://go.microsoft.com/fwlink/p/?linkid=17001">GetDC</a> function.)


## -returns



Returns the number of entries in the logical palette mapped to different values in the system palette. If an error occurs or no colors were updated, it returns zero.




## -remarks



To select the palette of the DrawDib DC as a background palette, use the <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> function and specify the DDF_BACKGROUNDPAL flag.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

