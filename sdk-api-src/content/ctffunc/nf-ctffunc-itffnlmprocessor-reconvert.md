---
UID: NF:ctffunc.ITfFnLMProcessor.Reconvert
title: ITfFnLMProcessor::Reconvert
author: windows-sdk-content
description: ITfFnLMProcessor::Reconvert method
old-location: tsf\itffnlmprocessor_reconvert.htm
tech.root: TSF
ms.assetid: 1580be2c-d16e-445b-83ba-c033eeb679b7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],Reconvert method, ITfFnLMProcessor.Reconvert, ITfFnLMProcessor::Reconvert, Reconvert, Reconvert method [Text Services Framework], Reconvert method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_reconvert_ref, ctffunc/ITfFnLMProcessor::Reconvert, tsf.itffnlmprocessor_reconvert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnLMProcessor.Reconvert
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnLMProcessor::Reconvert


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that covers the text to reconvert.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRange</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



This method is identical to <a href="https://msdn.microsoft.com/81d0f376-c059-4fcf-b85b-645bc98f957d">ITfFnReconversion::Reconvet</a>. When <b>ITfFnReconversion::Reconvet</b> is called in the text service, the text service should forward the call to this method if a language model processor is installed. If no language model processor is installed, the text service should perform its default processing.




## -see-also




<a href="https://msdn.microsoft.com/89581a75-9263-45d7-99de-b3bd78a5169c">ITfFnLMProcessor</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

