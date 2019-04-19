---
UID: NF:tapi3if.ITBasicCallControl.Transfer
title: ITBasicCallControl::Transfer (tapi3if.h)
author: windows-sdk-content
description: The Transfer method transfers the current call to the destination address.
old-location: tapi3\itbasiccallcontrol_transfer.htm
tech.root: Tapi
ms.assetid: 4f2a06e6-9f0b-4bf3-9f18-6e9f57c4b02f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Transfer method, ITBasicCallControl.Transfer, ITBasicCallControl::Transfer, Transfer, Transfer method [TAPI 2.2], Transfer method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_transfer, tapi3.itbasiccallcontrol_transfer, tapi3if/ITBasicCallControl::Transfer
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
 - ITBasicCallControl.Transfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITBasicCallControl::Transfer


## -description


The 
<b>Transfer</b> method transfers the current call to the destination address.


## -parameters




### -param pCall [in]

Pointer to 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> interface of consultation call created for the transfer.


### -param fSync [in]

Indicates whether the method should be completed synchronously (VARIANT_TRUE) or asynchronously (VARIANT_FALSE).


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter does not point to a valid call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Transfers not supported.

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



Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> or 
<a href="https://msdn.microsoft.com/fa5028f6-80eb-4076-a81c-c83b462fc27c">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> or 
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">ITSubStream::StartSubStream</a> following completion of the operation.

Call transfer involves setting up a consultation call in preparation for the transfer. <i>pCall</i> is the 
<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a> pointer returned by 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a> following the creation of a consultation call. 
<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">ITBasicCallControl::Finish</a> (FM_ASTRANSFER) completes the transfer.

If the consultation call is not in the CONNECTED state when 
<b>Transfer</b> is called, TAPI will use the destination address (as specified when the consultation call was first created via 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>) and try to connect at that time. If the original call had a <b>NULL</b> destination address, 
<b>Transfer</b> will fail with E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/73721921-c943-4adc-a2b1-e8c19ec809ac">Conference</a>



<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">Finish</a>



<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer Overview</a>
 

 

