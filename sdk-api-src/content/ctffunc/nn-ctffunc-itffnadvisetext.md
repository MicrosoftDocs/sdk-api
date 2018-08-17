---
UID: NN:ctffunc.ITfFnAdviseText
title: ITfFnAdviseText
author: windows-sdk-content
description: The ITfFnAdviseText interface is implemented by a text service and used by the TSF manager to supply notifications when the text or lattice element in a context changes.
old-location: tsf\itffnadvisetext.htm
old-project: TSF
ms.assetid: 7cca7f23-48d3-4855-8f3d-e937bbc990d4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnAdviseText, ITfFnAdviseText interface [Text Services Framework], ITfFnAdviseText interface [Text Services Framework],described, _tsf_itffnadvisetext_ref, ctffunc/ITfFnAdviseText, tsf.itffnadvisetext
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
 - ITfFnAdviseText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnAdviseText interface


## -description


The <b>ITfFnAdviseText</b> interface is implemented by a text service and used by the TSF manager to supply notifications when the text or lattice element in a context changes.

The manager obtains this interface from the text service by calling the text service <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnAdviseText.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnAdviseText</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnAdviseText</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnAdviseText</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c58f3d2f-ad74-43a7-a8a8-65d65d603611">OnLatticeUpdate</a>
</td>
<td align="left" width="63%">
Called when a lattice element within a context changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b8235bd-22a6-4074-89e5-2223a20f3559">OnTextUpdate</a>
</td>
<td align="left" width="63%">
Called when the text within a context changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

