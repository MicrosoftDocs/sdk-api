---
UID: NF:iwstdec.IAMWstDecoder.SetDrawBackgroundMode
title: IAMWstDecoder::SetDrawBackgroundMode (iwstdec.h)
author: windows-sdk-content
description: Downstream filters use the SetDrawBackgroundMode method to assign whether the caption text background is to be opaque or transparent.
old-location: dshow\iamwstdecoder_setdrawbackgroundmode.htm
tech.root: DirectShow
ms.assetid: d237d3dc-b3c9-44b2-9277-798c4830b361
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetDrawBackgroundMode method, IAMWstDecoder.SetDrawBackgroundMode, IAMWstDecoder::SetDrawBackgroundMode, IAMWstDecoderSetDrawBackgroundMode, SetDrawBackgroundMode, SetDrawBackgroundMode method [DirectShow], SetDrawBackgroundMode method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setdrawbackgroundmode, iwstdec/IAMWstDecoder::SetDrawBackgroundMode
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
 - IAMWstDecoder.SetDrawBackgroundMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWstDecoder::SetDrawBackgroundMode


## -description



Downstream filters use the <code>SetDrawBackgroundMode</code> method to assign whether the caption text background is to be opaque or transparent.




## -parameters




### -param Mode [in]

A member of the <a href="https://msdn.microsoft.com/en-us/library/Dd373506(v=VS.85).aspx">AM_WST_DRAWBGMODE</a> enumeration that specifies whether the caption text background is to be opaque or transparent.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_WST_DRAWBGMODE_Opaque</td>
<td>Caption text background is opaque.</td>
</tr>
<tr>
<td>AM_WST_DRAWBGMODE_Transparent</td>
<td>Caption text background is transparent.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376041(v=VS.85).aspx">IAMWstDecoder Interface</a>
 

 

