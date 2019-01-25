---
UID: NF:tapi3if.ITAddress.Forward
title: ITAddress::Forward
author: windows-sdk-content
description: The Forward method forwards calls destined for the address according to the forwarding instructions contained in ITForwardInformation. If pForwardInfo is set to NULL, forwarding is canceled.
old-location: tapi3\itaddress_forward.htm
tech.root: Tapi
ms.assetid: 4f070b50-db9a-49e8-a0f3-e448c5dee144
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Forward, Forward method [TAPI 2.2], Forward method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],Forward method, ITAddress.Forward, ITAddress::Forward, _tapi3_itaddress_forward, tapi3.itaddress_forward, tapi3if/ITAddress::Forward
ms.topic: method
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
 - ITAddress.Forward
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress::Forward


## -description


The 
Forward method forwards calls destined for the address according to the forwarding instructions contained in 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>. If <i>pForwardInfo</i> is set to <b>NULL</b>, forwarding is canceled.


## -parameters




### -param pForwardInfo [in]

Pointer to 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface, or set to <b>NULL</b> to cancel forwarding.


### -param pCall [in]

Pointer to 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface for the consultation call, if required by the telephony environment. May be <b>NULL</b> if not required.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The address does not support forwarding, or <i>pCall</i> does not point to a valid call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pForwardInfo</i> or <i>pCall</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">LineForward</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>
 




## -remarks



The information in <i>pForwardInfo</i> overrides any previous forwarding instructions.

If 
<a href="https://msdn.microsoft.com/4d3071d5-055a-469d-aa17-984b8210cbea">ITAddress::put_DoNotDisturb</a> is called with <i>fDoNotDisturb</i> set to VARIANT_FALSE, all forwarding is canceled.

An application can determine whether non-<b>NULL</b> consultation call is required by calling 
<a href="https://msdn.microsoft.com/76e61d5e-48b6-4b9c-9076-bd20a794859c">ITAddressCapabilities::get_AddressCapability</a> (AC_ADDRESSCAPFLAGS, <i>plCapability</i>) and checking whether the flag LINEADDRCAPFLAGS_FWDCONSULT, a member of 
<a href="https://msdn.microsoft.com/530af273-82ba-4310-8aac-266d657e1bfe">LINEADDRCAPFLAGS_ Constants</a>, has been set in <i>plCapability</i>. If it is set, a non-<b>NULL</b> value is required for the <i>pCall</i> parameter of the 
Forward method.

The 
Forward method is, in part, a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">LineForward</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/c70bf596-b2a4-46ec-9b1a-c9d948768b51">Forward overview</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">LineForward</a>
 

 

