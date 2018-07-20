---
UID: NF:tapi3if.ITAddress.put_DoNotDisturb
title: ITAddress::put_DoNotDisturb
author: windows-sdk-content
description: The put_DoNotDisturb method sets the do not disturb status. The do not disturb feature may not be available on all addresses.
old-location: tapi3\itaddress_put_donotdisturb.htm
old-project: tapi
ms.assetid: 4d3071d5-055a-469d-aa17-984b8210cbea
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAddress interface [TAPI 2.2],put_DoNotDisturb method, ITAddress.put_DoNotDisturb, ITAddress::put_DoNotDisturb, _tapi3_itaddress_put_donotdisturb, put_DoNotDisturb, put_DoNotDisturb method [TAPI 2.2], put_DoNotDisturb method [TAPI 2.2],ITAddress interface, tapi3.itaddress_put_donotdisturb, tapi3if/ITAddress::put_DoNotDisturb
ms.prod: windows
ms.technology: windows-sdk
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
 - ITAddress.put_DoNotDisturb
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::put_DoNotDisturb


## -description


The 
<b>put_DoNotDisturb</b> method sets the do not disturb status. The do not disturb feature may not be available on all addresses.


## -parameters




### -param fDoNotDisturb [in]

If VARIANT_TRUE, the do not disturb feature will be activated. If VARIANT_FALSE, the do not disturb feature will be deactivated and all forwarding canceled.


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
The <i>fDoNotDisturb</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -remarks



The DoNotDisturb feature is implemented using forwarding. If 
<b>put_DoNotDisturb</b> is called with VARIANT_TRUE, Tapi3.dll creates a 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a> list with the mode set to LINEFORWARDMODE_UNCOND and only one LINEFORWARD item with the destination address set to <b>NULL</b>. If 
<b>put_DoNotDisturb</b> is called with VARIANT_FALSE, Tapi3.dll cancels forwarding completely on this address, even those forwarding rules set with 
<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/d9257201-bcd1-4d6b-9bc7-24b323cd4f15">get_DoNotDisturb</a>
 

 

