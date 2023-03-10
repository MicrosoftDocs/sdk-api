---
UID: NF:tapi3if.ITBasicCallControl.ParkDirect
title: ITBasicCallControl::ParkDirect (tapi3if.h)
description: The ParkDirect method parks the call at a specified address.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","ParkDirect method","ITBasicCallControl.ParkDirect","ITBasicCallControl::ParkDirect","ParkDirect","ParkDirect method [TAPI 2.2]","ParkDirect method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_parkdirect","tapi3.itbasiccallcontrol_parkdirect","tapi3if/ITBasicCallControl::ParkDirect"]
old-location: tapi3\itbasiccallcontrol_parkdirect.htm
tech.root: tapi3
ms.assetid: 6461fd21-1726-4d24-8a17-d687b807b8e3
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],ParkDirect method, ITBasicCallControl.ParkDirect, ITBasicCallControl::ParkDirect, ParkDirect, ParkDirect method [TAPI 2.2], ParkDirect method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_parkdirect, tapi3.itbasiccallcontrol_parkdirect, tapi3if/ITBasicCallControl::ParkDirect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl::ParkDirect
 - tapi3if/ITBasicCallControl::ParkDirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.ParkDirect
---

# ITBasicCallControl::ParkDirect


## -description

The 
<b>ParkDirect</b> method parks the call at a specified address.

## -parameters

### -param pParkAddress [in]

Pointer to <b>BSTR</b> containing the address where the call is to be parked.

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
The <i>pParkAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Park is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pParkAddress</i> parameter is not valid.

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
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

With directed park, the application determines the address at which it wants to park the call. With 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect">ParkInDirect</a>, the switch determines the address and provides this to the application. In either case, a parked call can be unparked by specifying this address.

The parked call enters the disconnected state after it has been successfully parked.

Some switches can remind the user after a call has been parked for some long amount of time. The application sees an offering call with a call reason set to reminder.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pParkAddress</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/park-ovr">Park overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linepark">linePark</a>