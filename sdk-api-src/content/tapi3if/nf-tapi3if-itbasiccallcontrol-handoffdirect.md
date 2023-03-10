---
UID: NF:tapi3if.ITBasicCallControl.HandoffDirect
title: ITBasicCallControl::HandoffDirect (tapi3if.h)
description: The HandoffDirect method hands off the call to another application. This indicates that the application no longer requires ownership of the call.
helpviewer_keywords: ["HandoffDirect","HandoffDirect method [TAPI 2.2]","HandoffDirect method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","HandoffDirect method","ITBasicCallControl.HandoffDirect","ITBasicCallControl::HandoffDirect","_tapi3_itbasiccallcontrol_handoffdirect","tapi3.itbasiccallcontrol_handoffdirect","tapi3if/ITBasicCallControl::HandoffDirect"]
old-location: tapi3\itbasiccallcontrol_handoffdirect.htm
tech.root: tapi3
ms.assetid: a96a3790-ee5d-4983-b69a-30c7af96afd9
ms.date: 12/05/2018
ms.keywords: HandoffDirect, HandoffDirect method [TAPI 2.2], HandoffDirect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],HandoffDirect method, ITBasicCallControl.HandoffDirect, ITBasicCallControl::HandoffDirect, _tapi3_itbasiccallcontrol_handoffdirect, tapi3.itbasiccallcontrol_handoffdirect, tapi3if/ITBasicCallControl::HandoffDirect
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
 - ITBasicCallControl::HandoffDirect
 - tapi3if/ITBasicCallControl::HandoffDirect
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
 - ITBasicCallControl.HandoffDirect
---

# ITBasicCallControl::HandoffDirect


## -description

The 
<b>HandoffDirect</b> method hands off the call to another application. This indicates that the application no longer requires ownership of the call.

## -parameters

### -param pApplicationName [in]

Pointer to <b>BSTR</b> containing the specific application name to hand off call to. Can be full path name or executable name.

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
The <i>pApplicationName</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

If the receiving application has not opened the line for the media types involved in the call, the handoff will fail. If TAPI fails to hand off the call, TAPI will call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a>.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pApplicationName</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a>



<a href="/windows/desktop/Tapi/handoffs-ovr">Handoffs overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a>