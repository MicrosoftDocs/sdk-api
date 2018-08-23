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

The application or text service obtains this interface from a thread manager object by calling <a href="https://msdn.microsoft.com/en-us/library/ms628986(v=VS.85).aspx">ITfThreadMgr::GetFunctionProvider</a> with GUID_MASTERLM_FUNCTIONPROVIDER and then calling <a href="https://msdn.microsoft.com/en-us/library/ms538981(v=VS.85).aspx">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnLMProcessor. If <b>ITfThreadMgr::GetFunctionProvider</b> fails, then no language model processor is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnLMProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfFnLMProcessor</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms538946(v=VS.85).aspx">GetReconversion</a>
</td>
<td align="left" width="63%">
Obtains an ITfCandidateList object for a range from the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538947(v=VS.85).aspx">InvokeFunc</a>
</td>
<td align="left" width="63%">
Invokes a function of the language model text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538949(v=VS.85).aspx">InvokeKey</a>
</td>
<td align="left" width="63%">
Called to enable the language model text service to process a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538951(v=VS.85).aspx">QueryKey</a>
</td>
<td align="left" width="63%">
Called to determine if the language model text service handles a key event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538953(v=VS.85).aspx">QueryLangID</a>
</td>
<td align="left" width="63%">
Determines if the language model text service supports a particular language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538955(v=VS.85).aspx">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text that a reconversion applies to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538956(v=VS.85).aspx">Reconvert</a>
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



<a href="https://msdn.microsoft.com/en-us/library/ms628986(v=VS.85).aspx">ITfThreadMgr::GetFunctionProvider</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

