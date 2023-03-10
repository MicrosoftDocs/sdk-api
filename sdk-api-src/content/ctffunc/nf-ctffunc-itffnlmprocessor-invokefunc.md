---
UID: NF:ctffunc.ITfFnLMProcessor.InvokeFunc
title: ITfFnLMProcessor::InvokeFunc (ctffunc.h)
description: ITfFnLMProcessor::InvokeFunc method
helpviewer_keywords: ["ITfFnLMProcessor interface [Text Services Framework]","InvokeFunc method","ITfFnLMProcessor.InvokeFunc","ITfFnLMProcessor::InvokeFunc","InvokeFunc","InvokeFunc method [Text Services Framework]","InvokeFunc method [Text Services Framework]","ITfFnLMProcessor interface","_tsf_itffnlmprocessor_invokefunc_ref","ctffunc/ITfFnLMProcessor::InvokeFunc","tsf.itffnlmprocessor_invokefunc"]
old-location: tsf\itffnlmprocessor_invokefunc.htm
tech.root: TSF
ms.assetid: 9545c715-ec31-4360-b8f9-bb0746164878
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],InvokeFunc method, ITfFnLMProcessor.InvokeFunc, ITfFnLMProcessor::InvokeFunc, InvokeFunc, InvokeFunc method [Text Services Framework], InvokeFunc method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_invokefunc_ref, ctffunc/ITfFnLMProcessor::InvokeFunc, tsf.itffnlmprocessor_invokefunc
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnLMProcessor::InvokeFunc
 - ctffunc/ITfFnLMProcessor::InvokeFunc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnLMProcessor.InvokeFunc
---

# ITfFnLMProcessor::InvokeFunc


## -description

Invokes a function of the language model text service.

## -parameters

### -param pic [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface that represents context to perform the function on.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnlmprocessor">ITfFnLMProcessor</a>