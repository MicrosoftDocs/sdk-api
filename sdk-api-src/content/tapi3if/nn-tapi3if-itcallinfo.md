---
UID: NN:tapi3if.ITCallInfo
title: ITCallInfo (tapi3if.h)
author: windows-sdk-content
description: The ITCallInfo interface gets and sets a variety of information concerning a Call object. The ITAddress::get_Calls and IEnumCall::Next methods create the ITCallInfo interface.
old-location: tapi3\itcallinfo.htm
tech.root: Tapi
ms.assetid: 5209d4a1-e05b-453e-8896-2dc71f0b9af0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallInfo, ITCallInfo interface [TAPI 2.2], ITCallInfo interface [TAPI 2.2],described, _tapi3_itcallinfo, tapi3.itcallinfo, tapi3if/ITCallInfo
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
 - ITCallInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallInfo interface


## -description


The 
<b>ITCallInfo</b> interface gets and sets a variety of information concerning a 
<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call object</a>. The 
<a href="https://msdn.microsoft.com/b0b16578-0530-4ff9-a7ce-d36527ed2da9">ITAddress::get_Calls</a> and 
<a href="https://msdn.microsoft.com/5cb911fc-59aa-49c1-9df2-594b0dc22414">IEnumCall::Next</a> methods create the 
<b>ITCallInfo</b> interface.

The 
<a href="https://msdn.microsoft.com/20f7b20e-37f8-49f7-ae9d-83a9b9f574b6">ITCallInfo2</a> interface is an extension of the 
<b>ITCallInfo</b> interface. 
<b>ITCallInfo2</b> provides additional methods that allow an application to set event filtering on a per-call basis.

For a table showing the relationships between TAPI 2 functions and  
<b>ITCallInfo</b> methods, see 
<a href="https://msdn.microsoft.com/ae4f077b-ef6e-4ba4-b5db-bc749c2dcb9c">TAPI 2.x to TAPI 3.x Cross-Reference</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITCallInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f20f33-166f-4df7-9c9f-b7436958d16a">get_Address</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface of the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae7d74f7-c69b-45d1-a049-59e581856f27">get_CallHub</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface of the 
<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub object</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">get_CallInfoBuffer</a>
</td>
<td align="left" width="63%">
Gets call information items that require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">ITCallInfo::GetCallInfoBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c00e672-7bad-4a44-a76a-efd222f763d7">get_CallInfoLong</a>
</td>
<td align="left" width="63%">
Gets call information items described by a long, such as the bearer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/248022e7-c6cf-4c46-be94-ee1b79b9f39a">get_CallInfoString</a>
</td>
<td align="left" width="63%">
Gets call information items described by a string, such as the displayable address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7beb48f-d7d2-4a99-8e6a-6122059c9170">get_CallState</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a>, such as CS_IDLE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53">get_Privilege</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/8d2ab3d2-9531-40fc-910d-2bd81a075cc3">call privilege</a> of the application for the current call, such as CP_MONITOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">GetCallInfoBuffer</a>
</td>
<td align="left" width="63%">
Gets call information items that require a buffer, such as user-user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">put_CallInfoBuffer</a>
</td>
<td align="left" width="63%">
Sets call information items that require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">ITCallInfo::SetCallInfoBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5198b78-56f7-4964-970a-1068f2db4743">put_CallInfoLong</a>
</td>
<td align="left" width="63%">
Sets call information items described by a long, such as the bearer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22f1afb-e036-40d0-9a7f-61d8d24d2376">put_CallInfoString</a>
</td>
<td align="left" width="63%">
Sets call information items described by a string, such as the displayable address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/019823a3-e70d-4b0c-b996-07a13f2bd5f3">ReleaseUserUserInfo</a>
</td>
<td align="left" width="63%">
Releases the UUI buffer for this call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">SetCallInfoBuffer</a>
</td>
<td align="left" width="63%">
Sets call information items that require a buffer, such as user-user information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/20f7b20e-37f8-49f7-ae9d-83a9b9f574b6">ITCallInfo2</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>
 

 

