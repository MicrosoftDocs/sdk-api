---
UID: NN:tapi3if.ITForwardInformation
title: ITForwardInformation (tapi3if.h)
author: windows-sdk-content
description: The ITForwardInformation interface provides methods for setup and implementation of call forwarding.
old-location: tapi3\itforwardinformation.htm
tech.root: Tapi
ms.assetid: 0e06cd0b-b95b-4853-b883-53146be084f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITForwardInformation, ITForwardInformation interface [TAPI 2.2], ITForwardInformation interface [TAPI 2.2],described, _tapi3_itforwardinformation, tapi3.itforwardinformation, tapi3if/ITForwardInformation
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITForwardInformation"
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
 - ITForwardInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITForwardInformation interface


## -description


The 
<b>ITForwardInformation</b> interface provides methods for setup and implementation of call forwarding. The forward information object is created by 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>. A pointer to an existing forward information object can be retrieved using 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITForwardInformation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITForwardInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITForwardInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears all forwarding information in this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-get_forwardtypecaller">get_ForwardTypeCaller</a>
</td>
<td align="left" width="63%">
Gets the type of caller for a forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-get_forwardtypedestination">get_ForwardTypeDestination</a>
</td>
<td align="left" width="63%">
Gets the destination for a forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-get_numringsnoanswer">get_NumRingsNoAnswer</a>
</td>
<td align="left" width="63%">
Retrieves the number of rings after which a no answer condition is assumed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-getforwardtype">GetForwardType</a>
</td>
<td align="left" width="63%">
Gets the forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-put_numringsnoanswer">put_NumRingsNoAnswer</a>
</td>
<td align="left" width="63%">
Sets the number of rings after which a no answer condition is assumed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-setforwardtype">SetForwardType</a>
</td>
<td align="left" width="63%">
Sets the forwarding mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation2">ITForwardInformation2</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>
 

 

