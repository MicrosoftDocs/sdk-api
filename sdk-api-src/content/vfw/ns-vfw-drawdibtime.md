---
UID: NS:vfw.DRAWDIBTIME
title: DRAWDIBTIME
author: windows-sdk-content
description: The DRAWDIBTIME structure contains elapsed timing information for performing a set of DrawDib operations. The DrawDibTime function resets the count and the elapsed time value for each operation each time it is called.
old-location: multimedia\drawdibtime_struct.htm
old-project: Multimedia
ms.assetid: ec8a4e04-9e38-4db3-bb2b-838c63284f3a
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "*LPDRAWDIBTIME, DRAWDIBTIME, DRAWDIBTIME structure [Windows Multimedia], LPDRAWDIBTIME, LPDRAWDIBTIME structure pointer [Windows Multimedia], multimedia.drawdibtime_COLLISION618, multimedia.drawdibtime_struct, vfw/DRAWDIBTIME, vfw/LPDRAWDIBTIME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DRAWDIBTIME, *LPDRAWDIBTIME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - DRAWDIBTIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# DRAWDIBTIME structure


## -description



The <b>DRAWDIBTIME</b> structure contains elapsed timing information for performing a set of DrawDib operations. The <a href="https://msdn.microsoft.com/86dd2c5c-f853-4954-b245-6aa51d157600">DrawDibTime</a> function resets the count and the elapsed time value for each operation each time it is called.




## -struct-fields




### -field timeCount

Number of times the following operations have been performed since <a href="https://msdn.microsoft.com/86dd2c5c-f853-4954-b245-6aa51d157600">DrawDibTime</a> was last called:

<ul>
<li>Draw a bitmap on the screen.</li>
<li>Decompress a bitmap.</li>
<li>Dither a bitmap.</li>
<li>Stretch a bitmap.</li>
<li>Transfer bitmap data by using the <a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a> function.</li>
<li>Transfer bitmap data by using the <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> function.</li>
</ul>

### -field timeDraw


            Time to draw bitmaps.
          


### -field timeDecompress


            Time to decompress bitmaps.
          


### -field timeDither


            Time to dither bitmaps.
          


### -field timeStretch


            Time to stretch bitmaps.
          


### -field timeBlt


            Time to transfer bitmaps by using the <a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a> function.
          


### -field timeSetDIBits


            Time to transfer bitmaps by using the <a href="http://go.microsoft.com/fwlink/p/?linkid=17003">SetDIBits</a> function.
          


## -see-also




<a href="https://msdn.microsoft.com/c5e7237d-3a52-45b0-b6c5-13a1a8c1d50d">DrawDib</a>



<a href="https://msdn.microsoft.com/dde56eae-2f20-4c76-9d3d-8f8fe84217a9">DrawDib Structures</a>



<a href="https://msdn.microsoft.com/86dd2c5c-f853-4954-b245-6aa51d157600">DrawDibTime</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=17003">SetDIBits</a>
 

 

