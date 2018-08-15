---
UID: NN:ctffunc.ITfFnLMProcessor
title: ITfFnLMProcessor
author: windows-sdk-content
description: The ITfFnLMProcessor interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.
old-location: tsf\itffnlmprocessor.htm
old-project: TSF
ms.assetid: 89581a75-9263-45d7-99de-b3bd78a5169c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnLMProcessor, ITfFnLMProcessor interface [Text Services Framework], ITfFnLMProcessor interface [Text Services Framework],described, _tsf_itffnlmprocessor_ref, ctffunc/ITfFnLMProcessor, tsf.itffnlmprocessor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
 - ITfFnLMProcessor
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnLMProcessor interface


## -description


The <b>ITfFnLMProcessor</b> interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.

The application or text service obtains this interface from a thread manager object by calling <a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider</a> with GUID_MASTERLM_FUNCTIONPROVIDER and then calling <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnLMProcessor. If <b>ITfThreadMgr::GetFunctionProvider</b> fails, then no language model processor is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnLMProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnLMProcessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/21fcef3f-252c-4f67-a789-4527b8ee1b94">GetReconversion</a>
</td>
<td align="left" width="63%">
Obtains an ITfCandidateList object for a range from the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9545c715-ec31-4360-b8f9-bb0746164878">InvokeFunc</a>
</td>
<td align="left" width="63%">
Invokes a function of the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0611dd1e-6f79-4397-b523-e4fb278725f7">InvokeKey</a>
</td>
<td align="left" width="63%">
Called to enable the language model text service to process a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d28c2c2-ed0e-4987-ace9-25ed9d7a40a0">QueryKey</a>
</td>
<td align="left" width="63%">
Called to determine if the language model text service handles a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d645c1b-9ee6-47c4-8bbd-173e416f5688">QueryLangID</a>
</td>
<td align="left" width="63%">
Determines if the language model text service supports a particular language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84a9bf73-7215-429a-9573-66acf4d3ff18">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text that a reconversion applies to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1580be2c-d16e-445b-83ba-c033eeb679b7">Reconvert</a>
</td>
<td align="left" width="63%">
Invokes the reconversion process in the language model text service for a range.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">ITfCandidateList
      </a>



<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction
      </a>



<a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

