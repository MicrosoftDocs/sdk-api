---
UID: NN:ctffunc.ITfFnGetSAPIObject
title: ITfFnGetSAPIObject
author: windows-sdk-content
description: The ITfFnGetSAPIObject interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to obtain various SAPI objects.
old-location: tsf\itffngetsapiobject.htm
tech.root: TSF
ms.assetid: d7b4caa5-e915-4e57-878a-2a2d6ce609a7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfFnGetSAPIObject, ITfFnGetSAPIObject interface [Text Services Framework], ITfFnGetSAPIObject interface [Text Services Framework],described, _tsf_itffngetsapiobject_ref, ctffunc/ITfFnGetSAPIObject, tsf.itffngetsapiobject
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
 - ITfFnGetSAPIObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnGetSAPIObject interface


## -description


The <b>ITfFnGetSAPIObject</b> interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to obtain various SAPI objects.

A client obtains an instance of this interface by obtaining the <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> for the SAPI text service and calling <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with IID_ITfFnGetSAPIObject.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnGetSAPIObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnGetSAPIObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnGetSAPIObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dfa2bd2-e25c-4481-ab07-2f764434504d">Get</a>
</td>
<td align="left" width="63%">
Obtains a specified SAPI object.

</td>
</tr>
</table> 

