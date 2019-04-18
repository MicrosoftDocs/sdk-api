---
UID: NF:vfw.DrawDibGetPalette
title: DrawDibGetPalette function (vfw.h)
author: windows-sdk-content
description: The DrawDibGetPalette function retrieves the palette used by a DrawDib DC.
old-location: multimedia\drawdibgetpalette.htm
tech.root: Multimedia
ms.assetid: 38ed99a7-f704-467b-a23f-a19c990d0b10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawDibGetPalette, DrawDibGetPalette function [Windows Multimedia], _win32_DrawDibGetPalette, multimedia.drawdibgetpalette, vfw/DrawDibGetPalette
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
 - DrawDibGetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawDibGetPalette function


## -description



The <b>DrawDibGetPalette</b> function retrieves the palette used by a DrawDib DC.




## -parameters




### -param hdd

Handle to a DrawDib DC.


## -returns



Returns a handle to the palette if successful or <b>NULL</b> otherwise.




## -remarks



This function assumes the DrawDib DC contains a valid palette entry, implying that a call to this function must follow calls to the <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> or <a href="https://msdn.microsoft.com/89178e33-e440-49fe-9900-0baea229d289">DrawDibBegin</a> functions.

You should rarely need to call this function because you can realize the correct palette in response to a window message by using the <a href="https://msdn.microsoft.com/4723c8a4-36af-4543-b6df-d51f68a3e94d">DrawDibRealize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

