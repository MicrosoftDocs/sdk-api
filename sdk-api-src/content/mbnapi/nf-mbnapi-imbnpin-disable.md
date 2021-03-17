---
UID: NF:mbnapi.IMbnPin.Disable
title: IMbnPin::Disable (mbnapi.h)
description: Disables a PIN.
helpviewer_keywords: ["Disable","Disable method [Microsoft Broadband Networks]","Disable method [Microsoft Broadband Networks]","IMbnPin interface","IMbnPin interface [Microsoft Broadband Networks]","Disable method","IMbnPin.Disable","IMbnPin::Disable","mbn.imbnpin_disable","mbnapi/IMbnPin::Disable"]
old-location: mbn\imbnpin_disable.htm
tech.root: mbn
ms.assetid: 612edeb9-3de4-48ac-a311-7238402e8658
ms.date: 12/05/2018
ms.keywords: Disable, Disable method [Microsoft Broadband Networks], Disable method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],Disable method, IMbnPin.Disable, IMbnPin::Disable, mbn.imbnpin_disable, mbnapi/IMbnPin::Disable
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnPin::Disable
 - mbnapi/IMbnPin::Disable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPin.Disable
---

# IMbnPin::Disable


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Disables a PIN.

## -parameters

### -param pin [in]

The PIN value for the PIN type to be disabled.

### -param requestID [out]

A request ID set by the Mobile Broadband service to identify this asynchronous request.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  The Mobile Broadband device has probably been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
</table>

## -remarks

The <b>Disable</b> method disables the PIN type for a Mobile Broadband device. The <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pintype">PinType</a> property of this <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> represents the type of PIN to be deactivated for the device. <i>pin</i> contains the current value of PIN for the PIN type.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-ondisablecomplete">OnDisableComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>