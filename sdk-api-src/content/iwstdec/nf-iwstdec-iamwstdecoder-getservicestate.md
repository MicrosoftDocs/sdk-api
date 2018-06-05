---
UID: NF:iwstdec.IAMWstDecoder.GetServiceState
title: IAMWstDecoder::GetServiceState
author: windows-sdk-content
description: Applications use the GetServiceState method to retrieve the current service state.
old-location: dshow\iamwstdecoder_getservicestate.htm
old-project: DirectShow
ms.assetid: 7a927341-6ff4-41f5-918b-ea5b9e1ebe9a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetServiceState, GetServiceState method [DirectShow], GetServiceState method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetServiceState method, IAMWstDecoder.GetServiceState, IAMWstDecoder::GetServiceState, IAMWstDecoderGetServiceState, dshow.iamwstdecoder_getservicestate, iwstdec/IAMWstDecoder::GetServiceState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IAMWstDecoder.GetServiceState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::GetServiceState


## -description



Applications use the <code>GetServiceState</code> method to retrieve the current service state.




## -parameters




### -param lpState [out]

Pointer to a variable that receives the state, specified as a member of the <a href="https://msdn.microsoft.com/b6548144-7e18-4d5d-9243-51eb7db9821b">AM_WST_STATE</a> enumeration. The following values are possible.

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



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

