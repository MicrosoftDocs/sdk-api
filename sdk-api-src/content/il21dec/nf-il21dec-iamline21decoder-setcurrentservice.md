---
UID: NF:il21dec.IAMLine21Decoder.SetCurrentService
title: IAMLine21Decoder::SetCurrentService (il21dec.h)
author: windows-sdk-content
description: The SetCurrentService method sets the closed captioning service.
old-location: dshow\iamline21decoder_setcurrentservice.htm
tech.root: DirectShow
ms.assetid: 2f1945c3-644d-4e72-b2b7-a7e068b59d96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetCurrentService method, IAMLine21Decoder.SetCurrentService, IAMLine21Decoder::SetCurrentService, IAMLine21DecoderSetCurrentService, SetCurrentService, SetCurrentService method [DirectShow], SetCurrentService method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setcurrentservice, il21dec/IAMLine21Decoder::SetCurrentService
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
 - IAMLine21Decoder.SetCurrentService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMLine21Decoder::SetCurrentService


## -description



The <code>SetCurrentService</code> method sets the closed captioning service.




## -parameters




### -param Service

Member of the <a href="https://msdn.microsoft.com/en-us/library/Dd373474(v=VS.85).aspx">AM_LINE21_CCSERVICE</a> enumeration that specifies the closed captioning service. The default service is CC1.


## -returns



<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument</td>
</tr>
<tr>
<td>E_NOTIMPL</td>
<td>The requested service is not implemented.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389385(v=VS.85).aspx">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389387(v=VS.85).aspx">IAMLine21Decoder::GetCurrentService</a>
 

 

