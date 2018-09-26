---
UID: NN:tapi3if.ITBasicCallControl2
title: ITBasicCallControl2
author: windows-sdk-content
description: The ITBasicCallControl2 interface is an extension of the ITBasicCallControl interface.
old-location: tapi3\itbasiccallcontrol2.htm
tech.root: tapi
ms.assetid: fc693221-b7ba-4b33-aed7-59ec92fc9b58
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITBasicCallControl2, ITBasicCallControl2 interface [TAPI 2.2], ITBasicCallControl2 interface [TAPI 2.2],described, _tapi3_itbasiccallcontrol2, tapi3.itbasiccallcontrol2, tapi3if/ITBasicCallControl2
ms.prod: windows
ms.technology: windows-sdk
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
 - ITBasicCallControl2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl2 interface


## -description


The 
<b>ITBasicCallControl2</b> interface is an extension of the 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface. 
<b>ITBasicCallControl2</b> supplies additional methods that allow an application to select a terminal onto a call. The 
<b>ITBasicCallControl2</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicCallControl2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITBasicCallControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITBasicCallControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20b7266c-8990-457c-94cf-18cc2bed6b21">RequestTerminal</a>
</td>
<td align="left" width="63%">
Gets a suitable terminal, given the class, media, and direction required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87117ec1-0d61-4edb-8ed6-0d029a77e1a5">SelectTerminalOnCall</a>
</td>
<td align="left" width="63%">
Selects a terminal onto the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93795757-58b6-4eb5-9d0c-f7c0a3bb9695">UnselectTerminalOnCall</a>
</td>
<td align="left" width="63%">
Unselects a terminal from the call.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>
 

 

