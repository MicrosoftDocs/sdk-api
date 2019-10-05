---
UID: NN:ctffunc.ITfFnPlayBack
title: ITfFnPlayBack (ctffunc.h)
author: windows-sdk-content
description: The ITfFnPlayBack interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.
old-location: tsf\itffnplayback.htm
tech.root: TSF
ms.assetid: e9a0d1a3-70c9-4816-8cd4-f2574392953e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnPlayBack, ITfFnPlayBack interface [Text Services Framework], ITfFnPlayBack interface [Text Services Framework],described, _tsf_itffnplayback_ref, ctffunc/ITfFnPlayBack, tsf.itffnplayback
ms.topic: interface
f1_keywords: 
 - "ctffunc/ITfFnPlayBack"
dev_langs:
 - c++
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
 - ITfFnPlayBack
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnPlayBack interface


## -description


The <b>ITfFnPlayBack</b> interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.

Each spoken word or phrase has audio data stored with the text. This interface is used to obtain the range that covers the spoken text and to play back the audio data.

A client obtains an instance of this interface by obtaining the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> for the SAPI text service and calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPlayBack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnPlayBack</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnPlayBack</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnplayback-play">Play</a>
</td>
<td align="left" width="63%">
Causes the audio data for a range of text to be played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnplayback-queryrange">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text for a word or phrase that contains audio data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

