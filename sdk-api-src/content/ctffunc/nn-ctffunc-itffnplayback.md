---
UID: NN:ctffunc.ITfFnPlayBack
title: ITfFnPlayBack
author: windows-sdk-content
description: The ITfFnPlayBack interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.
old-location: tsf\itffnplayback.htm
old-project: TSF
ms.assetid: e9a0d1a3-70c9-4816-8cd4-f2574392953e
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfFnPlayBack, ITfFnPlayBack interface [Text Services Framework], ITfFnPlayBack interface [Text Services Framework],described, _tsf_itffnplayback_ref, ctffunc/ITfFnPlayBack, tsf.itffnplayback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITfFnPlayBack
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnPlayBack interface


## -description


The <b>ITfFnPlayBack</b> interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.

Each spoken word or phrase has audio data stored with the text. This interface is used to obtain the range that covers the spoken text and to play back the audio data.

A client obtains an instance of this interface by obtaining the <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> for the SAPI text service and calling <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPlayBack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnPlayBack</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnPlayBack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnPlayBack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9945bc65-fe9f-42d1-ade1-db016dc7489c">Play</a>
</td>
<td align="left" width="63%">
Causes the audio data for a range of text to be played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6113703-5515-4f1a-8e2e-1373077dafc2">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text for a word or phrase that contains audio data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider
      </a>



<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">
        ITfFunctionProvider::GetFunction
      </a>



<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

