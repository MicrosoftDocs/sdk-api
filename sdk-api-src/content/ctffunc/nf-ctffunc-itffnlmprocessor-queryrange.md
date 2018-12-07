---
UID: NF:ctffunc.ITfFnLMProcessor.QueryRange
title: ITfFnLMProcessor::QueryRange
author: windows-sdk-content
description: ITfFnLMProcessor::QueryRange method
old-location: tsf\itffnlmprocessor_queryrange.htm
tech.root: TSF
ms.assetid: 84a9bf73-7215-429a-9573-66acf4d3ff18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],QueryRange method, ITfFnLMProcessor.QueryRange, ITfFnLMProcessor::QueryRange, QueryRange, QueryRange method [Text Services Framework], QueryRange method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_queryrange_ref, ctffunc/ITfFnLMProcessor::QueryRange, tsf.itffnlmprocessor_queryrange
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
 - ITfFnLMProcessor.QueryRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnLMProcessor::QueryRange


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> object that covers all or part of the text to be reconverted.


### -param ppNewRange [out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> pointer that receives a range object that covers all of the text that can be reconverted. If none of the text covered by <i>pRange</i> can be reconverted, this parameters receives <b>NULL</b>. In this case, the method will return S_OK; the caller must verify that this parameter is not <b>NULL</b> before using the pointer.

This parameter is optional and can be <b>NULL</b>. In this case, the range is not required.


### -param pfAccepted [out]

Pointer to a <b>BOOL</b> value that receives zero if none of the text covered by <i>pRange</i> can be reconverted or nonzero otherwise.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



This method is identical to <a href="https://msdn.microsoft.com/en-us/library/ms538973(v=VS.85).aspx">ITfFnReconversion::QueryRange</a>. When <b>ITfFnReconversion::QueryRange</b> is called in the text service, the text service should forward the call to this method if a language model processor is installed. If no language model processor is installed, the text service should perform its default processing.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538944(v=VS.85).aspx">ITfFnLMProcessor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms538973(v=VS.85).aspx">ITfFnReconversion::QueryRange</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

