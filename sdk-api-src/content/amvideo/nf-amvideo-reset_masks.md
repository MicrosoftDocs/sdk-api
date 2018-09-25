---
UID: NF:amvideo.RESET_MASKS
title: RESET_MASKS macro
author: windows-sdk-content
description: The RESET_MASKS macro fills the color mask fields in a VIDEOINFO structure with zeroes.
old-location: dshow\reset_masks.htm
tech.root: DirectShow
ms.assetid: 039a43c1-c795-4374-ada8-2ea611c6409a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: RESET_MASKS, RESET_MASKS macro [DirectShow], amvideo/RESET_MASKS, dshow.reset_masks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: amvideo.h
req.include-header: Streams.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Amvideo.h
api_name:
 - RESET_MASKS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RESET_MASKS macro


## -description



The <b>RESET_MASKS</b> macro fills the color mask fields in a <a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a> structure with zeroes.




## -parameters




### -param pbmi

Pointer to a <a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a> structure.


## -remarks



As defined in the header file Amvideo.h, this macro is not correct and will cause a compile error. Replace it with the following:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#undef RESET_MASKS
#define RESET_MASKS(x) (ZeroMemory((PVOID)(x)-&gt;dwBitMasks, SIZE_MASKS))
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/02401edc-362b-4f6c-b10b-c46b30b3ebe7">Video and Image Functions</a>
 

 

