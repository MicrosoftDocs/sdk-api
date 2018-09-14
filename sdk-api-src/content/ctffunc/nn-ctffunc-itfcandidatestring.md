---
UID: NN:ctffunc.ITfCandidateString
title: ITfCandidateString
author: windows-sdk-content
description: The ITfCandidateString interface is implemented by a text service and is used by the TSF manager or a client to obtain information about a candidate string object.
old-location: tsf\itfcandidatestring.htm
tech.root: TSF
ms.assetid: 82c77b59-a50c-42ae-ba1d-25a1c196662d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfCandidateString, ITfCandidateString interface [Text Services Framework], ITfCandidateString interface [Text Services Framework],described, _tsf_itfcandidatestring_ref, ctffunc/ITfCandidateString, tsf.itfcandidatestring
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfCandidateString
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCandidateString interface


## -description


The <b>ITfCandidateString</b> interface is implemented by a text service and is used by the TSF manager or a client to obtain information about a candidate string object.

The TSF manager implements this interface to provide access to this interface to other clients. This enables the TSF manager to function as a mediator between the client and the text service.

To obtain an instance of this interface, the TSF manager or client can call <a href="https://msdn.microsoft.com/4cb2127c-cce5-4815-b40b-e6e15058eab5">ITfCandidateList::GetCandidate</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateString</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCandidateString</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCandidateString</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ec9a89-db57-41ad-9e32-db0b24abda13">GetIndex</a>
</td>
<td align="left" width="63%">
Obtains the index of the candidate string object within the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/157dc848-858c-462f-8e41-78d6bfe20705">GetString</a>
</td>
<td align="left" width="63%">
Obtains the text of the candidate string object.

</td>
</tr>
</table> 

