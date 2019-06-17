---
UID: NS:vfw.__unnamed_struct_12
title: DRAWDIBTIME (vfw.h)
author: windows-sdk-content
description: The DRAWDIBTIME structure contains elapsed timing information for performing a set of DrawDib operations. The DrawDibTime function resets the count and the elapsed time value for each operation each time it is called.
old-location: multimedia\drawdibtime_struct.htm
tech.root: Multimedia
ms.assetid: ec8a4e04-9e38-4db3-bb2b-838c63284f3a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDRAWDIBTIME, DRAWDIBTIME, DRAWDIBTIME structure [Windows Multimedia], LPDRAWDIBTIME, LPDRAWDIBTIME structure pointer [Windows Multimedia], multimedia.drawdibtime_COLLISION618, multimedia.drawdibtime_struct, vfw/DRAWDIBTIME, vfw/LPDRAWDIBTIME"
ms.topic: struct
f1_keywords: ["vfw/DRAWDIBTIME"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: DRAWDIBTIME, *LPDRAWDIBTIME
req.redist: 
ms.custom: 19H1
---

# DRAWDIBTIME structure


## -description



The <b>DRAWDIBTIME</b> structure contains elapsed timing information for performing a set of DrawDib operations. The <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibtime">DrawDibTime</a> function resets the count and the elapsed time value for each operation each time it is called.




## -struct-fields




### -field timeCount

Number of times the following operations have been performed since <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibtime">DrawDibTime</a> was last called:

<ul>
<li>Draw a bitmap on the screen.</li>
<li>Decompress a bitmap.</li>
<li>Dither a bitmap.</li>
<li>Stretch a bitmap.</li>
<li>Transfer bitmap data by using the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> function.</li>
<li>Transfer bitmap data by using the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> function.</li>
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

Time to transfer bitmaps by using the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> function.
          


### -field timeSetDIBits

Time to transfer bitmaps by using the <a href="http://go.microsoft.com/fwlink/p/?linkid=17003">SetDIBits</a> function.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/drawdib">DrawDib</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/drawdib-structures">DrawDib Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibtime">DrawDibTime</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=17003">SetDIBits</a>
 

 

