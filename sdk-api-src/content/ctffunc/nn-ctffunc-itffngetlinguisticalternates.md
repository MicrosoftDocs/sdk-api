---
UID: NN:ctffunc.ITfFnGetLinguisticAlternates
title: ITfFnGetLinguisticAlternates (ctffunc.h)
author: windows-sdk-content
description: The ITfFnGetLinguisticAlternates interface is implemented by a text service and/or by the TSF manager to provide linguistic alternates for the text within a given range passed as a parameter.
old-location: tsf\itffngetlinguisticalternates.htm
tech.root: TSF
ms.assetid: 854FB6EC-CEF1-4FB6-AA5F-34B26B46A3CA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnGetLinguisticAlternates, ITfFnGetLinguisticAlternates interface [Text Services Framework], ITfFnGetLinguisticAlternates interface [Text Services Framework],described, ctffunc/ITfFnGetLinguisticAlternates, tsf.itffngetlinguisticalternates
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnGetLinguisticAlternates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfFnGetLinguisticAlternates interface


## -description


The <b>ITfFnGetLinguisticAlternates</b> interface is implemented by a text service and/or by the TSF manager to provide linguistic alternates for the text within a given range passed as a parameter.

Apps can use this interface to obtain IME alternates for a text range; therefore the interface <b>ITfFnGetLinguisticAlternates</b>, along with <a href="https://msdn.microsoft.com/5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF">ITfFnSearchCandidateProvider</a>, provides a TSF-based replacement for the <a href="https://msdn.microsoft.com/c38547fa-b9d8-41a0-8d73-21056212b775">ImmGetConversionList</a> function.  Typically IMEs implement either <b>ITfFnGetLinguisticAlternates</b> or <b>ITfFnSearchCandidateProvider</b> (or neither).

An app obtains a pointer to this interface by calling TSF manager <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> method with <b>IID_ITfFnGetLinguisticAlternates</b>.


<div class="alert"><b>Note</b>  This interface may not be supported for all IMEs. There may be differences in support between IMEs on the Desktop and IMEs in the new Windows UI on Windows 8.1.  Some IMEs instead implement the related interface <a href="https://msdn.microsoft.com/5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF">ITfFnSearchCandidateProvider</a> that can be used as a substitute for this API.  Suggested app usage is to check for this interface first, and if it's not available then check if <b>ITfFnSearchCandidateProvider</b> is supported instead.  IMEs that wish to maintain compatibility with Windows 8 should implement <b>ITfFnSearchCandidateProvider</b> instead.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnGetLinguisticAlternates</b> interface inherits from <a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction</a>. <b>ITfFnGetLinguisticAlternates</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnGetLinguisticAlternates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17BB0DF8-3F97-423C-A2FD-CDC7590EE49B">GetAlternates</a>
</td>
<td align="left" width="63%">
Returns a list of alternate strings for a given text range.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction</a>
 

 

