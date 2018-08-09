---
UID: NN:ctffunc.ITfFnSearchCandidateProvider
title: ITfFnSearchCandidateProvider
author: windows-sdk-content
description: Enables an integrated search experience in an Input Method Editor (IME).
old-location: tsf\itffnsearchcandidateprovider.htm
old-project: TSF
ms.assetid: 5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnSearchCandidateProvider, ITfFnSearchCandidateProvider interface [Text Services Framework], ITfFnSearchCandidateProvider interface [Text Services Framework],described, ctffunc/ITfFnSearchCandidateProvider, tsf.itffnsearchcandidateprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Ctffunc.h
api_name:
 - ITfFnSearchCandidateProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnSearchCandidateProvider interface


## -description


 Enables an integrated search experience in an Input Method Editor (IME).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnSearchCandidateProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnSearchCandidateProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnSearchCandidateProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7D7E8171-229F-4D9C-B086-D68E064A8A4C">GetSearchCandidates</a>
</td>
<td align="left" width="63%">
Gets a list of conversion candidates for a given string without generating any IME-related messages or events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C4DA0D3-58FD-4955-9658-29ECD8FECEC1">SetResult</a>
</td>
<td align="left" width="63%">
Provides a text Service or IME with history data when a candidate is chosen by the user.

</td>
</tr>
</table> 


## -remarks



Implement the <b>ITfFnSearchCandidateProvider</b> interface in your Input Method Editor (IME) to enable an integrated search experience. Implementing this interface enables searches with meaningful results to begin before IME input has been completed, by providing a set of possible IME conversion candidates for a given input string.  Apps can use this interface to obtain IME conversions for a string, so the <b>ITfFnSearchCandidateProvider</b> interface, along with <a href="https://msdn.microsoft.com/854FB6EC-CEF1-4FB6-AA5F-34B26B46A3CA">ITfFnGetLinguisticAlternates</a>, provides a TSF-based replacement for the <a href="https://msdn.microsoft.com/c38547fa-b9d8-41a0-8d73-21056212b775">ImmGetConversionList</a> function.  Typically IMEs implement either <b>ITfFnGetLinguisticAlternates</b> or <b>ITfFnSearchCandidateProvider</b> (or neither).

Call <a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">GetFunctionProvider</a> with the CLSID of a text service to get an <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> instance.  Use the following call to the <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> method to get the <b>ITfFnSearchCandidateProvider</b> interface pointer.

<code>ITfFunctionProvider::GetFunction(GUID_NULL, IID_ITfFnSearchCandidateProvider, &amp;pSearchCandidate)</code>




## -see-also




<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">GetFunction</a>



<a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">GetFunctionProvider</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/7cb7c94c-1526-48e1-9ab0-068e03a462c7">SearchPaneQueryLinguisticDetails</a>
 

 

