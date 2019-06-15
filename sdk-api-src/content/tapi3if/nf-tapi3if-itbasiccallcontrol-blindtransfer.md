---
UID: NF:tapi3if.ITBasicCallControl.BlindTransfer
title: ITBasicCallControl::BlindTransfer (tapi3if.h)
author: windows-sdk-content
description: The BlindTransfer method performs a blind or single-step transfer of the specified call to the specified destination address. The application must be the owner of the call. After a successful transfer, the call state transitions to CS_DISCONNECTED.
old-location: tapi3\itbasiccallcontrol_blindtransfer.htm
tech.root: Tapi
ms.assetid: 766a48af-512a-4ad6-99e1-436141bf8447
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BlindTransfer, BlindTransfer method [TAPI 2.2], BlindTransfer method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],BlindTransfer method, ITBasicCallControl.BlindTransfer, ITBasicCallControl::BlindTransfer, _tapi3_itbasiccallcontrol_blindtransfer, tapi3.itbasiccallcontrol_blindtransfer, tapi3if/ITBasicCallControl::BlindTransfer
ms.topic: method
f1_keywords: ["tapi3if/ITBasicCallControl.BlindTransfer"]
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
 - ITBasicCallControl.BlindTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITBasicCallControl::BlindTransfer


## -description


The 
<b>BlindTransfer</b> method performs a blind or single-step transfer of the specified call to the specified destination address. The application must be the owner of the call. After a successful transfer, the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a> transitions to CS_DISCONNECTED.


## -parameters




### -param pDestAddress [in]

Pointer to <b>BSTR</b> containing destination address for the transfer.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDestAddress</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Blind transfer is not supported.

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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

The application must use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

In some cases, the application may need to use the address translation interfaces (
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>) to obtain a <i>pDestAddress</i> string in the proper format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/transfer-ovr">Transfer Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>
 

 

