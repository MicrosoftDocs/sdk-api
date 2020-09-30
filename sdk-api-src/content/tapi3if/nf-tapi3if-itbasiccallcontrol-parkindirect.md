---
UID: NF:tapi3if.ITBasicCallControl.ParkIndirect
title: ITBasicCallControl::ParkIndirect (tapi3if.h)
description: The ParkIndirect method parks the call and returns the parked address.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","ParkIndirect method","ITBasicCallControl.ParkIndirect","ITBasicCallControl::ParkIndirect","ParkIndirect","ParkIndirect method [TAPI 2.2]","ParkIndirect method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_parkindirect","tapi3.itbasiccallcontrol_parkindirect","tapi3if/ITBasicCallControl::ParkIndirect"]
old-location: tapi3\itbasiccallcontrol_parkindirect.htm
tech.root: tapi3
ms.assetid: 661ad11c-b653-4b70-9553-59d484527c29
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],ParkIndirect method, ITBasicCallControl.ParkIndirect, ITBasicCallControl::ParkIndirect, ParkIndirect, ParkIndirect method [TAPI 2.2], ParkIndirect method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_parkindirect, tapi3.itbasiccallcontrol_parkindirect, tapi3if/ITBasicCallControl::ParkIndirect
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
 - ITBasicCallControl::ParkIndirect
 - tapi3if/ITBasicCallControl::ParkIndirect
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
 - ITBasicCallControl.ParkIndirect
---

# ITBasicCallControl::ParkIndirect


## -description

The 
<b>ParkIndirect</b> method parks the call and returns the parked address.

## -parameters

### -param ppNonDirAddress [out]

Pointer to a <b>BSTR</b> representation of the address where the call was parked.

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
The <i>ppNonDirAddress</i> parameter is not a valid pointer.

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
The <i>ppNonDirAddress</i> parameter is not valid.

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

With 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect">ParkDirect</a>, the application determines the address at which it wants to park the call. With nondirected park, the switch determines the address and provides this to the application. In either case, a parked call can be unparked by specifying this address.

The parked call enters the disconnected state after it has been successfully parked.

Some switches can remind the user after a call has been parked for some long amount of time. The application sees an offering call with a call reason set to reminder.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppNonDirAddress</i> parameter.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/park-ovr">Park overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linepark">linePark</a>