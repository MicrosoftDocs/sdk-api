---
UID: NF:ctffunc.ITfFnLMProcessor.InvokeFunc
title: ITfFnLMProcessor::InvokeFunc
author: windows-sdk-content
description: ITfFnLMProcessor::InvokeFunc method
old-location: tsf\itffnlmprocessor_invokefunc.htm
old-project: TSF
ms.assetid: 9545c715-ec31-4360-b8f9-bb0746164878
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],InvokeFunc method, ITfFnLMProcessor.InvokeFunc, ITfFnLMProcessor::InvokeFunc, InvokeFunc, InvokeFunc method [Text Services Framework], InvokeFunc method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_invokefunc_ref, ctffunc/ITfFnLMProcessor::InvokeFunc, tsf.itffnlmprocessor_invokefunc
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
 - ITfFnLMProcessor.InvokeFunc
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnLMProcessor::InvokeFunc


## -description




## -parameters




### -param pic [in]

Pointer to an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface that represents context to perform the function on.


### -param refguidFunc [in]

Contains a GUID that specifies the function to invoke. Possible values for this parameter are defined by the language model text service provider.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/89581a75-9263-45d7-99de-b3bd78a5169c">ITfFnLMProcessor</a>
 

 

