---
UID: NF:iwstdec.IAMWstDecoder.GetServiceState
title: IAMWstDecoder::GetServiceState (iwstdec.h)
author: windows-sdk-content
description: Applications use the GetServiceState method to retrieve the current service state.
old-location: dshow\iamwstdecoder_getservicestate.htm
tech.root: DirectShow
ms.assetid: 7a927341-6ff4-41f5-918b-ea5b9e1ebe9a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetServiceState, GetServiceState method [DirectShow], GetServiceState method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetServiceState method, IAMWstDecoder.GetServiceState, IAMWstDecoder::GetServiceState, IAMWstDecoderGetServiceState, dshow.iamwstdecoder_getservicestate, iwstdec/IAMWstDecoder::GetServiceState
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
 - IAMWstDecoder.GetServiceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWstDecoder::GetServiceState


## -description



Applications use the <code>GetServiceState</code> method to retrieve the current service state.




## -parameters




### -param lpState [out]

Pointer to a variable that receives the state, specified as a member of the <a href="https://msdn.microsoft.com/en-us/library/Dd373510(v=VS.85).aspx">AM_WST_STATE</a> enumeration. The following values are possible.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_WST_STATE_On</td>
<td>The WST service is on.</td>
</tr>
<tr>
<td>AM_WST_STATE_Off</td>
<td>The WST service is off.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376041(v=VS.85).aspx">IAMWstDecoder Interface</a>
 

 

