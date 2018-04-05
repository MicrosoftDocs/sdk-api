---
UID: NF:iwstdec.IAMWstDecoder.SetRedrawAlways
title: IAMWstDecoder::SetRedrawAlways method
author: windows-driver-content
description: Downstream filters use the SetRedrawAlways method to determine whether the whole output bitmap should be redrawn for each sample.
old-location: dshow\iamwstdecoder_setredrawalways.htm
old-project: DirectShow
ms.assetid: 4663a9c0-3d08-4f25-8742-458081536f98
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMWstDecoder, IAMWstDecoder interface [DirectShow], SetRedrawAlways method, IAMWstDecoder::SetRedrawAlways, IAMWstDecoderSetRedrawAlways, SetRedrawAlways method [DirectShow], SetRedrawAlways method [DirectShow], IAMWstDecoder interface, SetRedrawAlways,IAMWstDecoder.SetRedrawAlways, dshow.iamwstdecoder_setredrawalways, iwstdec/IAMWstDecoder::SetRedrawAlways
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_WST_STYLE, *PAM_WST_STYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMWstDecoder.SetRedrawAlways
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::SetRedrawAlways method


## -description



Downstream filters use the <code>SetRedrawAlways</code> method to determine whether the whole output bitmap should be redrawn for each sample.




## -parameters




### -param bOption [in]

Specifies a <b>BOOL</b> to assign whether the whole output bitmap should be redrawn for each sample.

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
<td>Redraw the whole output bitmap for each sample.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Do not redraw the whole output bitmap for each sample.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

