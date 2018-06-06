---
UID: NN:tapi3if.ITCallHub
title: ITCallHub
author: windows-sdk-content
description: The ITCallHub interface provides methods to retrieve information concerning a CallHub object. The IEnumCallHub::Next and ITTapi::get_CallHubs methods create the ITCallHub interface.
old-location: tapi3\itcallhub.htm
old-project: Tapi
ms.assetid: bdc91cac-c0ec-4484-a415-8cd1aa1e18e8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITCallHub, ITCallHub interface [TAPI 2.2], ITCallHub interface [TAPI 2.2],described, _tapi3_itcallhub, tapi3.itcallhub, tapi3if/ITCallHub
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallHub
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallHub interface


## -description


The 
<b>ITCallHub</b> interface provides methods to retrieve information concerning a CallHub object. The 
<a href="https://msdn.microsoft.com/16469c1c-f12f-4941-9fd4-1413620c89bd">IEnumCallHub::Next</a> and 
<a href="https://msdn.microsoft.com/57177526-1351-4f59-8f24-74d8b87d27c0">ITTapi::get_CallHubs</a> methods create the 
<b>ITCallHub</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallHub</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITCallHub</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Attempts to remove all calls and participants from Call Hub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/becacf70-0ae7-419c-a53f-c6172278d29f">EnumerateCalls</a>
</td>
<td align="left" width="63%">
Enumerates calls currently associated with the call hub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56634ab6-b905-48bb-a4d1-7ca1f0c4c0cf">get_Calls</a>
</td>
<td align="left" width="63%">
Creates a collection of calls associated with the current call hub. This method is provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52313969-ce8e-43da-8844-b4d0834dd446">get_NumCalls</a>
</td>
<td align="left" width="63%">
Gets the number of calls currently in the CallHub.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ca4bbad-6822-4a8b-8df4-da6e630752f0">get_State</a>
</td>
<td align="left" width="63%">
Gets the current state of the CallHub.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

