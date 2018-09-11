---
UID: NF:tapi3if.ITBasicCallControl.Unpark
title: ITBasicCallControl::Unpark
author: windows-sdk-content
description: The Unpark method gets the call from park.
old-location: tapi3\itbasiccallcontrol_unpark.htm
tech.root: tapi
ms.assetid: d4cea44e-0dac-4021-a42c-b136c2e686e0
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Unpark method, ITBasicCallControl.Unpark, ITBasicCallControl::Unpark, Unpark, Unpark method [TAPI 2.2], Unpark method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_unpark, tapi3.itbasiccallcontrol_unpark, tapi3if/ITBasicCallControl::Unpark
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITBasicCallControl.Unpark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl::Unpark


## -description


The 
<b>Unpark</b> method gets the call from park.


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The park operation is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
Call state must be CS_IDLE.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



To unpark a call, 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">CreateCall</a> must be called using as the destination address the current parked location of the call. See the example below.


#### Examples

<pre class="syntax" xml:space="preserve"><code>// Note: the parameters used in this call are obtained from elsewhere in the code.  

HRESULT hr = pAddress-&gt;CreateCall( bstrAddressToCall, 
                           dwAddressType, 
                           dwMediaTypes, 
                           &amp;pBasicCall 
                           ); 
// If ( hr != S_OK ) process the error here. 

// Select appropriate terminals for call, and then call: 
pBasicCall -&gt;Unpark();</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/6a82f03e-d8fd-4d0b-8f5d-f7934ba86759">Park overview</a>



<a href="https://msdn.microsoft.com/6461fd21-1726-4d24-8a17-d687b807b8e3">ParkDirect</a>



<a href="https://msdn.microsoft.com/661ad11c-b653-4b70-9553-59d484527c29">ParkIndirect</a>



<a href="https://msdn.microsoft.com/9262ab44-eac7-43e2-a0ec-dceea0838b09">lineUnpark</a>
 

 

