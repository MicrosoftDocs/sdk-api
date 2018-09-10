---
UID: NF:il21dec.IAMLine21Decoder.SetBackgroundColor
title: IAMLine21Decoder::SetBackgroundColor
author: windows-sdk-content
description: The SetBackgroundColor method sets the background color that the Line 21 Decoder filter uses for overlay. The default background color is magenta.
old-location: dshow\iamline21decoder_setbackgroundcolor.htm
tech.root: DirectShow
ms.assetid: a69bb0d0-5afb-420f-a97c-071dc472e1d2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetBackgroundColor method, IAMLine21Decoder.SetBackgroundColor, IAMLine21Decoder::SetBackgroundColor, IAMLine21DecoderSetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DirectShow], SetBackgroundColor method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setbackgroundcolor, il21dec/IAMLine21Decoder::SetBackgroundColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: il21dec.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMLine21Decoder.SetBackgroundColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMLine21Decoder::SetBackgroundColor


## -description



The <code>SetBackgroundColor</code> method sets the background color that the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter uses for overlay. The default background color is magenta.



Generally, applications should not call this method. The background color must match the overlay color key, which is defined by the downstream rendering filter.


## -parameters




### -param dwPhysColor

Sets the background color as a pixel color value. The meaning of the pixel value is defined by the bit depth of the filter's current output format.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/ba75dc5b-207e-4425-a8fe-8da16fc89921">IAMLine21Decoder::GetBackgroundColor</a>
 

 

