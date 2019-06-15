---
UID: NN:ctffunc.ITfCandidateList
title: ITfCandidateList (ctffunc.h)
author: windows-sdk-content
description: The ITfCandidateList interface is implemented by a text service and is used by the TSF manager or a client (application or other text service) to obtain and manipulate candidate string objects.
old-location: tsf\itfcandidatelist.htm
tech.root: TSF
ms.assetid: e41ba461-6337-4feb-ba16-3942920ebb9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCandidateList, ITfCandidateList interface [Text Services Framework], ITfCandidateList interface [Text Services Framework],described, _tsf_itfcandidatelist_ref, ctffunc/ITfCandidateList, tsf.itfcandidatelist
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateList
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCandidateList interface


## -description


The <b>ITfCandidateList</b> interface is implemented by a text service and is used by the TSF manager or a client (application or other text service) to obtain and manipulate candidate string objects.

The TSF manager implements this interface to provide access to this interface to other clients. This enables the TSF manager to function as a mediator between the client and the text service.

To obtain an instance of this interface the TSF manager or client can call <a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCandidateList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCandidateList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-enumcandidates">EnumCandidates</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all the candidate string objects in the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-getcandidate">GetCandidate</a>
</td>
<td align="left" width="63%">
Obtains a specific candidate string object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-getcandidatenum">GetCandidateNum</a>
</td>
<td align="left" width="63%">
Obtains the number of candidate string objects in the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-setresult">SetResult</a>
</td>
<td align="left" width="63%">
Specifies the result of a reconversion operation for s specific candidate string.

</td>
</tr>
</table> 


## -remarks



When a text service must interpret text before it is inserted into a context, there might be more than one possible interpretation of the text. Speech input is an example of this. If the spoken word is "there", other possible interpretations might be "their" or "they're". The text service will insert the most appropriate text, but there is still some chance of error involved. Text reconversion is the process of allowing the user to select alternate text for the inserted text. The alternate text objects are known as candidates.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

