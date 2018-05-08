---
UID: NN:ctffunc.ITfFnReconversion
title: ITfFnReconversion
author: windows-driver-content
description: The ITfFnReconversion interface is implemented by a text service and is used by the TSF manager or a client to support reconversion of text provided by the text service.
old-location: tsf\itffnreconversion.htm
old-project: TSF
ms.assetid: deb5c007-58d5-4bae-92eb-a05675f5dfac
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfFnReconversion, ITfFnReconversion interface [Text Services Framework], ITfFnReconversion interface [Text Services Framework],described, _tsf_itffnreconversion_ref, ctffunc/ITfFnReconversion, tsf.itffnreconversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFnReconversion
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnReconversion interface


## -description


The <b>ITfFnReconversion</b> interface is implemented by a text service and is used by the TSF manager or a client to support reconversion of text provided by the text service.

The TSF manager implements this interface to provide access to this interface to other clients. This allows the TSF manager to function as a mediator between the client and the text service.

The TSF manager obtains this interface by calling the text service <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> method with IID_ITfFnReconversion.

An application obtains this interface by calling the TSF manager <b>ITfFunctionProvider::GetFunction</b> method with IID_ITfFnReconversion.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnReconversion</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnReconversion</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ed696088-c599-4c83-968e-d09d9ae81c10">GetReconversion</a>
</td>
<td align="left" width="63%">
Obtains an ITfCandidateList object for a range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/022d0ad7-5359-48df-b83b-2319eb1a84bf">QueryRange</a>
</td>
<td align="left" width="63%">
Obtains the range of text that the reconversion applies to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81d0f376-c059-4fcf-b85b-645bc98f957d">Reconvert</a>
</td>
<td align="left" width="63%">
Invokes the reconversion process for a range of text.

</td>
</tr>
</table> 


## -remarks



When a text service must interpret text before it is inserted into a context, there might be more than one possible interpretation of the text. Speech input is an example of this. If the spoken word is "there", other possible interpretations might be "their" or "they're". The text service will insert the most appropriate text, but there is still some chance of error involved. Text reconversion is the process of allowing the user to select alternate text for the inserted text.



