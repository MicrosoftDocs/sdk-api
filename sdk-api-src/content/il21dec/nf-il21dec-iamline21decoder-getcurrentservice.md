---
UID: NF:il21dec.IAMLine21Decoder.GetCurrentService
title: IAMLine21Decoder::GetCurrentService
author: windows-sdk-content
description: The GetCurrentService method retrieves the current closed captioning service.
old-location: dshow\iamline21decoder_getcurrentservice.htm
old-project: DirectShow
ms.assetid: bfd1c33d-27e0-4923-9c80-5d1bedb4fd25
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetCurrentService, GetCurrentService method [DirectShow], GetCurrentService method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetCurrentService method, IAMLine21Decoder.GetCurrentService, IAMLine21Decoder::GetCurrentService, IAMLine21DecoderGetCurrentService, dshow.iamline21decoder_getcurrentservice, il21dec/IAMLine21Decoder::GetCurrentService
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMLine21Decoder::GetCurrentService


## -description



The <code>GetCurrentService</code> method retrieves the current closed captioning service.




## -parameters




### -param lpService

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/dd2b618f-ffbf-4d48-bbe8-6d237a0f54e8">AM_LINE21_CCSERVICE</a> enumeration. The default service is CC1.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/2f1945c3-644d-4e72-b2b7-a7e068b59d96">IAMLine21Decoder::SetCurrentService</a>
 

 

