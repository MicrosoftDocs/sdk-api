---
UID: NN:tapi3if.IEnumCall
title: IEnumCall (tapi3if.h)
author: windows-sdk-content
description: The IEnumCall interface provides COM-standard enumeration methods for the ITCallInfo interface. The ITCallHub::EnumerateCalls and ITAddress::EnumerateCalls methods return a pointer to IEnumCall.
old-location: tapi3\ienumcall.htm
tech.root: Tapi
ms.assetid: 418c1005-98f0-406f-a85c-c08adb269b9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumCall, IEnumCall interface [TAPI 2.2], IEnumCall interface [TAPI 2.2],described, _tapi3_ienumcall, tapi3.ienumcall, tapi3if/IEnumCall
ms.topic: interface
f1_keywords: 
 - "tapi3if/IEnumCall"
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
 - IEnumCall
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumCall interface


## -description


The 
<b>IEnumCall</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-enumeratecalls">ITCallHub::EnumerateCalls</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-enumeratecalls">ITAddress::EnumerateCalls</a> methods return a pointer to 
<b>IEnumCall</b>.

The 
<b>IEnumCall</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCall</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>
 

 

