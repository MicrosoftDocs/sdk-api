---
UID: NF:il21dec.IAMLine21Decoder.SetRedrawAlways
title: IAMLine21Decoder::SetRedrawAlways
author: windows-sdk-content
description: The SetRedrawAlways method specifies whether the Line 21 Decoder filter redraws the entire output bitmap for each sample.
old-location: dshow\iamline21decoder_setredrawalways.htm
old-project: DirectShow
ms.assetid: 20f2e95a-8362-457d-b562-f7263e698551
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetRedrawAlways method, IAMLine21Decoder.SetRedrawAlways, IAMLine21Decoder::SetRedrawAlways, IAMLine21DecoderSetRedrawAlways, SetRedrawAlways, SetRedrawAlways method [DirectShow], SetRedrawAlways method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setredrawalways, il21dec/IAMLine21Decoder::SetRedrawAlways
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMLine21Decoder.SetRedrawAlways
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMLine21Decoder::SetRedrawAlways


## -description



The <code>SetRedrawAlways</code> method specifies whether the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter redraws the entire output bitmap for each sample.




## -parameters




### -param bOption

Specifies one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The filter always redraws the entire bitmap.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The filter does not always redraw the entire bitmap. (Default)</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



Generally, applications should not call this method. The downstream mixer or renderer filter should call this method with the value <b>TRUE</b> if it writes into the buffers that it receives from the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter. Redrawing degrades performance and increases CPU load, because it negates any potential optimizations.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/9ab65d23-816d-4c6f-a0bc-b3334babdc23">IAMLine21Decoder::GetRedrawAlways</a>
 

 

