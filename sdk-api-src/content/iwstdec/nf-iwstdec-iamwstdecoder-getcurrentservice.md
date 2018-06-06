---
UID: NF:iwstdec.IAMWstDecoder.GetCurrentService
title: IAMWstDecoder::GetCurrentService
author: windows-sdk-content
description: Applications use the GetCurrentService method to retrieve the current WST service.
old-location: dshow\iamwstdecoder_getcurrentservice.htm
old-project: DirectShow
ms.assetid: d16b3501-efee-48e6-8d5d-d76f206d77ed
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetCurrentService, GetCurrentService method [DirectShow], GetCurrentService method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetCurrentService method, IAMWstDecoder.GetCurrentService, IAMWstDecoder::GetCurrentService, IAMWstDecoderGetCurrentService, dshow.iamwstdecoder_getcurrentservice, iwstdec/IAMWstDecoder::GetCurrentService
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder.GetCurrentService
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::GetCurrentService


## -description



Applications use the <code>GetCurrentService</code> method to retrieve the current WST service.




## -parameters




### -param lpService [out]

Specifies a pointer to an <a href="https://msdn.microsoft.com/63c20aff-eb30-44fd-bc8d-e155d7014f73">AM_WST_SERVICE</a> enumeration to receive the service currently being used.

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
<td>AM_WST_SERVICE_None</td>
<td>No service is currently available.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_Text</td>
<td>The service is providing text.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_IDS</td>
<td>The service is providing IDS data.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_Invalid</td>
<td>The service is invalid.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

