---
UID: NN:ctffunc.ITfFnLMProcessor
title: ITfFnLMProcessor (ctffunc.h)
author: windows-sdk-content
description: The ITfFnLMProcessor interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.
old-location: tsf\itffnlmprocessor.htm
tech.root: TSF
ms.assetid: 89581a75-9263-45d7-99de-b3bd78a5169c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor, ITfFnLMProcessor interface [Text Services Framework], ITfFnLMProcessor interface [Text Services Framework],described, _tsf_itffnlmprocessor_ref, ctffunc/ITfFnLMProcessor, tsf.itffnlmprocessor
ms.topic: interface
f1_keywords: 
 - "ctffunc/ITfFnLMProcessor"
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
 - ITfFnLMProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnLMProcessor interface


## -description


The <b>ITfFnLMProcessor</b> interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.

The application or text service obtains this interface from a thread manager object by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a> with GUID_MASTERLM_FUNCTIONPROVIDER and then calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnLMProcessor. If <b>ITfThreadMgr::GetFunctionProvider</b> fails, then no language model processor is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnLMProcessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnLMProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnLMProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-getreconversion">GetReconversion</a>
</td>
<td align="left" width="63%">
Obtains an ITfCandidateList object for a range from the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-invokefunc">InvokeFunc</a>
</td>
<td align="left" width="63%">
Invokes a function of the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-invokekey">InvokeKey</a>
</td>
<td align="left" width="63%">
Called to enable the language model text service to process a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-querykey">QueryKey</a>
</td>
<td align="left" width="63%">
Called to determine if the language model text service handles a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-querylangid">QueryLangID</a>
</td>
<td align="left" width="63%">
Determines if the language model text service supports a particular language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-queryrange">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text that a reconversion applies to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnlmprocessor-reconvert">Reconvert</a>
</td>
<td align="left" width="63%">
Invokes the reconversion process in the language model text service for a range.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatelist">ITfCandidateList
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

