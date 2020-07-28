---
UID: NN:ctffunc.ITfFnReconversion
title: ITfFnReconversion (ctffunc.h)
description: The ITfFnReconversion interface is implemented by a text service and is used by the TSF manager or a client to support reconversion of text provided by the text service.
helpviewer_keywords: ["ITfFnReconversion","ITfFnReconversion interface [Text Services Framework]","ITfFnReconversion interface [Text Services Framework]","described","_tsf_itffnreconversion_ref","ctffunc/ITfFnReconversion","tsf.itffnreconversion"]
old-location: tsf\itffnreconversion.htm
tech.root: TSF
ms.assetid: deb5c007-58d5-4bae-92eb-a05675f5dfac
ms.date: 12/05/2018
ms.keywords: ITfFnReconversion, ITfFnReconversion interface [Text Services Framework], ITfFnReconversion interface [Text Services Framework],described, _tsf_itffnreconversion_ref, ctffunc/ITfFnReconversion, tsf.itffnreconversion
f1_keywords:
- ctffunc/ITfFnReconversion
dev_langs:
- c++
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
- ITfFnReconversion
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnReconversion interface


## -description


The <b>ITfFnReconversion</b> interface is implemented by a text service and is used by the TSF manager or a client to support reconversion of text provided by the text service.

The TSF manager implements this interface to provide access to this interface to other clients. This allows the TSF manager to function as a mediator between the client and the text service.

The TSF manager obtains this interface by calling the text service <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> method with IID_ITfFnReconversion.

An application obtains this interface by calling the TSF manager <b>ITfFunctionProvider::GetFunction</b> method with IID_ITfFnReconversion.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnReconversion</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnReconversion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnReconversion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">GetReconversion</a>
</td>
<td align="left" width="63%">
Obtains an ITfCandidateList object for a range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text that the reconversion applies to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-reconvert">Reconvert</a>
</td>
<td align="left" width="63%">
Invokes the reconversion process for a range of text.

</td>
</tr>
</table> 


## -remarks



When a text service must interpret text before it is inserted into a context, there might be more than one possible interpretation of the text. Speech input is an example of this. If the spoken word is "there", other possible interpretations might be "their" or "they're". The text service will insert the most appropriate text, but there is still some chance of error involved. Text reconversion is the process of allowing the user to select alternate text for the inserted text.



