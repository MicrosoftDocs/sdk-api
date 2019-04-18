---
UID: NN:ctffunc.ITfFnPropertyUIStatus
title: ITfFnPropertyUIStatus (ctffunc.h)
author: windows-sdk-content
description: The ITfFnPropertyUIStatus interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.
old-location: tsf\itffnpropertyuistatus.htm
tech.root: TSF
ms.assetid: 5583ae98-02a5-4303-9674-b8a85b52442a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnPropertyUIStatus, ITfFnPropertyUIStatus interface [Text Services Framework], ITfFnPropertyUIStatus interface [Text Services Framework],described, _tsf_itffnpropertyuistatus_ref, ctffunc/ITfFnPropertyUIStatus, tsf.itffnpropertyuistatus
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
 - ITfFnPropertyUIStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnPropertyUIStatus interface


## -description


The <b>ITfFnPropertyUIStatus</b> interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.

An application or text service obtains an instance of this interface by obtaining the <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> for the text service and calling <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPropertyUIStatus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnPropertyUIStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnPropertyUIStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnPropertyUIStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aef8c1b4-3cda-4fa3-ae8c-a8f8da4840b5">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a text service property UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817329fb-521a-426a-88d8-b36ee161b6b9">SetStatus</a>
</td>
<td align="left" width="63%">
Modifies the status of a text service property UI.

</td>
</tr>
</table> 

