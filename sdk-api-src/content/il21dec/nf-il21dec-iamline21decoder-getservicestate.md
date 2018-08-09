---
UID: NF:il21dec.IAMLine21Decoder.GetServiceState
title: IAMLine21Decoder::GetServiceState
author: windows-sdk-content
description: The GetServiceState method indicates whether closed captioning is on or off.
old-location: dshow\iamline21decoder_getservicestate.htm
old-project: DirectShow
ms.assetid: c88d2328-0338-4c0b-b719-8501bcbb8a69
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetServiceState, GetServiceState method [DirectShow], GetServiceState method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetServiceState method, IAMLine21Decoder.GetServiceState, IAMLine21Decoder::GetServiceState, IAMLine21DecoderGetServiceState, dshow.iamline21decoder_getservicestate, il21dec/IAMLine21Decoder::GetServiceState
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
 - IAMLine21Decoder.GetServiceState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMLine21Decoder::GetServiceState


## -description



The <code>GetServiceState</code> method indicates whether closed captioning is on or off.




## -parameters




### -param lpState

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/fdd1dec4-660c-46d0-b18c-b725b813c6a7">AM_LINE21_CCSTATE</a> enumeration.


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
 




## -remarks



By default, the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> enables closed captioning.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/009e7d14-5946-42f0-8832-7fd8c565a877">IAMLine21Decoder::SetServiceState</a>
 

 

