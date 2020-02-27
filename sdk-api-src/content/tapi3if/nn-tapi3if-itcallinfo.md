---
UID: NN:tapi3if.ITCallInfo
title: ITCallInfo (tapi3if.h)
description: The ITCallInfo interface gets and sets a variety of information concerning a Call object. The ITAddress::get_Calls and IEnumCall::Next methods create the ITCallInfo interface.
old-location: tapi3\itcallinfo.htm
tech.root: Tapi
ms.assetid: 5209d4a1-e05b-453e-8896-2dc71f0b9af0
ms.date: 12/05/2018
ms.keywords: ITCallInfo, ITCallInfo interface [TAPI 2.2], ITCallInfo interface [TAPI 2.2],described, _tapi3_itcallinfo, tapi3.itcallinfo, tapi3if/ITCallInfo
f1_keywords:
- tapi3if/ITCallInfo
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
- ITCallInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallInfo interface


## -description


The 
<b>ITCallInfo</b> interface gets and sets a variety of information concerning a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call object</a>. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_calls">ITAddress::get_Calls</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-next">IEnumCall::Next</a> methods create the 
<b>ITCallInfo</b> interface.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2">ITCallInfo2</a> interface is an extension of the 
<b>ITCallInfo</b> interface. 
<b>ITCallInfo2</b> provides additional methods that allow an application to set event filtering on a per-call basis.

For a table showing the relationships between TAPI 2 functions and  
<b>ITCallInfo</b> methods, see 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-x-to-tapi-3-x-cross-reference">TAPI 2.x to TAPI 3.x Cross-Reference</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_address">get_Address</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address object</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callhub">get_CallHub</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/callhub-object">CallHub object</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">get_CallInfoBuffer</a>
</td>
<td align="left" width="63%">
Gets call information items that require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">ITCallInfo::GetCallInfoBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong">get_CallInfoLong</a>
</td>
<td align="left" width="63%">
Gets call information items described by a long, such as the bearer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring">get_CallInfoString</a>
</td>
<td align="left" width="63%">
Gets call information items described by a string, such as the displayable address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callstate">get_CallState</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a>, such as CS_IDLE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege">get_Privilege</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_privilege">call privilege</a> of the application for the current call, such as CP_MONITOR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">GetCallInfoBuffer</a>
</td>
<td align="left" width="63%">
Gets call information items that require a buffer, such as user-user information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">put_CallInfoBuffer</a>
</td>
<td align="left" width="63%">
Sets call information items that require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">ITCallInfo::SetCallInfoBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong">put_CallInfoLong</a>
</td>
<td align="left" width="63%">
Sets call information items described by a long, such as the bearer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfostring">put_CallInfoString</a>
</td>
<td align="left" width="63%">
Sets call information items described by a string, such as the displayable address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo">ReleaseUserUserInfo</a>
</td>
<td align="left" width="63%">
Releases the UUI buffer for this call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">SetCallInfoBuffer</a>
</td>
<td align="left" width="63%">
Sets call information items that require a buffer, such as user-user information.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2">ITCallInfo2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetcallstatus">lineGetCallStatus</a>
 

 

