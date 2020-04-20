---
UID: NN:tapi3if.ITCallHub
title: ITCallHub (tapi3if.h)
description: The ITCallHub interface provides methods to retrieve information concerning a CallHub object. The IEnumCallHub::Next and ITTapi::get_CallHubs methods create the ITCallHub interface.helpviewer_keywords: ["ITCallHub","ITCallHub interface [TAPI 2.2]","ITCallHub interface [TAPI 2.2]","described","_tapi3_itcallhub","tapi3.itcallhub","tapi3if/ITCallHub"]
old-location: tapi3\itcallhub.htm
tech.root: Tapi
ms.assetid: bdc91cac-c0ec-4484-a415-8cd1aa1e18e8
ms.date: 12/05/2018
ms.keywords: ITCallHub, ITCallHub interface [TAPI 2.2], ITCallHub interface [TAPI 2.2],described, _tapi3_itcallhub, tapi3.itcallhub, tapi3if/ITCallHub
f1_keywords:
- tapi3if/ITCallHub
dev_langs:
- c++
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
- ITCallHub
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallHub interface


## -description


The 
<b>ITCallHub</b> interface provides methods to retrieve information concerning a CallHub object. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcallhub-next">IEnumCallHub::Next</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_callhubs">ITTapi::get_CallHubs</a> methods create the 
<b>ITCallHub</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallHub</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallHub</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallHub</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-clear">Clear</a>
</td>
<td align="left" width="63%">
Attempts to remove all calls and participants from Call Hub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-enumeratecalls">EnumerateCalls</a>
</td>
<td align="left" width="63%">
Enumerates calls currently associated with the call hub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_calls">get_Calls</a>
</td>
<td align="left" width="63%">
Creates a collection of calls associated with the current call hub. This method is provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_numcalls">get_NumCalls</a>
</td>
<td align="left" width="63%">
Gets the number of calls currently in the CallHub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_state">get_State</a>
</td>
<td align="left" width="63%">
Gets the current state of the CallHub.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

