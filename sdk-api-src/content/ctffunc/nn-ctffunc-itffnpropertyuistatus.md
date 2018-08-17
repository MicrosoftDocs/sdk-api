---
UID: NN:ctffunc.ITfFnPropertyUIStatus
title: ITfFnPropertyUIStatus
author: windows-sdk-content
description: The ITfFnPropertyUIStatus interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.
old-location: tsf\itffnpropertyuistatus.htm
old-project: TSF
ms.assetid: 5583ae98-02a5-4303-9674-b8a85b52442a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnPropertyUIStatus, ITfFnPropertyUIStatus interface [Text Services Framework], ITfFnPropertyUIStatus interface [Text Services Framework],described, _tsf_itffnpropertyuistatus_ref, ctffunc/ITfFnPropertyUIStatus, tsf.itffnpropertyuistatus
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
 - ITfFnPropertyUIStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnPropertyUIStatus interface


## -description


The <b>ITfFnPropertyUIStatus</b> interface is implemented by a text service and used by an application or text service to obtain and set the status of the text service property UI.

An application or text service obtains an instance of this interface by obtaining the <a href="https://msdn.microsoft.com/en-us/library/ms538979(v=VS.85).aspx">ITfFunctionProvider</a> for the text service and calling <a href="https://msdn.microsoft.com/en-us/library/ms538981(v=VS.85).aspx">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPropertyUIStatus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnPropertyUIStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfFnPropertyUIStatus</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms538965(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a text service property UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538967(v=VS.85).aspx">SetStatus</a>
</td>
<td align="left" width="63%">
Modifies the status of a text service property UI.

</td>
</tr>
</table> 

