---
UID: NF:il21dec.IAMLine21Decoder.GetCurrentService
title: IAMLine21Decoder::GetCurrentService (il21dec.h)
author: windows-sdk-content
description: The GetCurrentService method retrieves the current closed captioning service.
old-location: dshow\iamline21decoder_getcurrentservice.htm
tech.root: DirectShow
ms.assetid: bfd1c33d-27e0-4923-9c80-5d1bedb4fd25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentService, GetCurrentService method [DirectShow], GetCurrentService method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetCurrentService method, IAMLine21Decoder.GetCurrentService, IAMLine21Decoder::GetCurrentService, IAMLine21DecoderGetCurrentService, dshow.iamline21decoder_getcurrentservice, il21dec/IAMLine21Decoder::GetCurrentService
ms.topic: method
f1_keywords: 
 - "il21dec/IAMLine21Decoder.GetCurrentService"
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
 - IAMLine21Decoder.GetCurrentService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMLine21Decoder::GetCurrentService


## -description



The <code>GetCurrentService</code> method retrieves the current closed captioning service.




## -parameters




### -param lpService

Pointer to a variable that receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/il21dec/ne-il21dec-_am_line21_ccservice">AM_LINE21_CCSERVICE</a> enumeration. The default service is CC1.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setcurrentservice">IAMLine21Decoder::SetCurrentService</a>
 

 

