---
UID: NF:ctffunc.ITfFnLMProcessor.GetReconversion
title: ITfFnLMProcessor::GetReconversion
author: windows-sdk-content
description: ITfFnLMProcessor::GetReconversion method
old-location: tsf\itffnlmprocessor_getreconversion.htm
old-project: TSF
ms.assetid: 21fcef3f-252c-4f67-a789-4527b8ee1b94
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetReconversion, GetReconversion method [Text Services Framework], GetReconversion method [Text Services Framework],ITfFnLMProcessor interface, ITfFnLMProcessor interface [Text Services Framework],GetReconversion method, ITfFnLMProcessor.GetReconversion, ITfFnLMProcessor::GetReconversion, _tsf_itffnlmprocessor_getreconversion_ref, ctffunc/ITfFnLMProcessor::GetReconversion, tsf.itffnlmprocessor_getreconversion
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnLMProcessor.GetReconversion
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnLMProcessor::GetReconversion


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that covers the text to be reconverted. To obtain this range object, call <a href="https://msdn.microsoft.com/022d0ad7-5359-48df-b83b-2319eb1a84bf">ITfFnReconversion::QueryRange</a>.


### -param ppCandList [out]

Pointer to an <b>ITfCandidateList</b> pointer that receives the candidate list object.


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



This method is identical to <a href="https://msdn.microsoft.com/ed696088-c599-4c83-968e-d09d9ae81c10">ITfFnReconversion::GetReconversion</a>. When <b>ITfFnReconversion::GetReconversion</b> is called in the text service, the text service should forward the call to this method if a language model processor is installed. If no language model processor is installed, the text service should perform its default processing.




## -see-also




<a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">ITfCandidateList
      </a>



<a href="https://msdn.microsoft.com/89581a75-9263-45d7-99de-b3bd78a5169c">ITfFnLMProcessor</a>



<a href="https://msdn.microsoft.com/ed696088-c599-4c83-968e-d09d9ae81c10">ITfFnReconversion::GetReconversion
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

