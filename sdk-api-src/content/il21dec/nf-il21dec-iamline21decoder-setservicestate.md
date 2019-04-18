---
UID: NF:il21dec.IAMLine21Decoder.SetServiceState
title: IAMLine21Decoder::SetServiceState (il21dec.h)
author: windows-sdk-content
description: The SetServiceState method enables or disables closed captions.
old-location: dshow\iamline21decoder_setservicestate.htm
tech.root: DirectShow
ms.assetid: 009e7d14-5946-42f0-8832-7fd8c565a877
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetServiceState method, IAMLine21Decoder.SetServiceState, IAMLine21Decoder::SetServiceState, IAMLine21DecoderSetServiceState, SetServiceState, SetServiceState method [DirectShow], SetServiceState method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setservicestate, il21dec/IAMLine21Decoder::SetServiceState
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
 - IAMLine21Decoder.SetServiceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMLine21Decoder::SetServiceState


## -description



The <code>SetServiceState</code> method enables or disables closed captions.




## -parameters




### -param State

Member of the <a href="https://msdn.microsoft.com/en-us/library/Dd373475(v=VS.85).aspx">AM_LINE21_CCSTATE</a> enumeration, specify whether to enable or disable closed captions.


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



<a href="https://msdn.microsoft.com/en-us/library/Dd389385(v=VS.85).aspx">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389392(v=VS.85).aspx">IAMLine21Decoder::GetServiceState</a>
 

 

