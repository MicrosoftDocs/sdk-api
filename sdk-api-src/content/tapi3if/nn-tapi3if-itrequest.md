---
UID: NN:tapi3if.ITRequest
title: ITRequest
author: windows-sdk-content
description: The ITRequest interface allows an application to use Assisted Telephony. Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.
old-location: tapi3\itrequest.htm
tech.root: tapi
ms.assetid: 2b6d4f99-3ffe-44ce-9cb5-3fdd565085db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITRequest, ITRequest interface [TAPI 2.2], ITRequest interface [TAPI 2.2],described, _tapi3_itrequest, tapi3.itrequest, tapi3if/ITRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRequest interface


## -description


The 
<b>ITRequest</b> interface allows an application to use 
<a href="https://msdn.microsoft.com/1c41f52b-f8bf-410e-a966-9323a690a4d5">Assisted Telephony</a>. Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.

The Request object must be created using COM <b>CoCreateInstance</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITRequest</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6896a18a-75ff-4f43-81e2-7b828bb16ff6">MakeCall</a>
</td>
<td align="left" width="63%">
Makes call to designated party.

</td>
</tr>
</table> 

