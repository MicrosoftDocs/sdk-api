---
UID: NF:mbnapi.IMbnPin.Unblock
title: IMbnPin::Unblock (mbnapi.h)
description: Unblocks a blocked PIN.
helpviewer_keywords: ["IMbnPin interface [Microsoft Broadband Networks]","Unblock method","IMbnPin.Unblock","IMbnPin::Unblock","Unblock","Unblock method [Microsoft Broadband Networks]","Unblock method [Microsoft Broadband Networks]","IMbnPin interface","mbn.imbnpin_unblock","mbnapi/IMbnPin::Unblock"]
old-location: mbn\imbnpin_unblock.htm
tech.root: mbn
ms.assetid: 7e5ec24c-681c-4259-9f6a-949bf40d5b3e
ms.date: 12/05/2018
ms.keywords: IMbnPin interface [Microsoft Broadband Networks],Unblock method, IMbnPin.Unblock, IMbnPin::Unblock, Unblock, Unblock method [Microsoft Broadband Networks], Unblock method [Microsoft Broadband Networks],IMbnPin interface, mbn.imbnpin_unblock, mbnapi/IMbnPin::Unblock
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
 - IMbnPin::Unblock
 - mbnapi/IMbnPin::Unblock
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
 - IMbnPin.Unblock
---

# IMbnPin::Unblock


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Unblocks a blocked PIN.

## -parameters

### -param puk [in]

The password unblock key (PUK) value for this PIN type.

### -param newPin [in]

A new PIN to be set for this PIN type.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This method is not allowed for calling process privileges.

</td>
</tr>
</table>

## -remarks

The <b>Unblock</b> method unblocks the PIN for the pin type by entering the PUK and sets a new PIN. The <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pintype">PinType</a> property of this <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> represents the type of PIN which is being changed.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-onunblockcomplete">OnUnblockComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>.

Whenever the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> results with the current PIN state set to <b>MBN_PIN_STATE_UNBLOCK</b>, then the application should use <b>Unblock</b> on the PIN type which is returned in <b>PinInfo.pinType</b> passed by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-ongetpinstatecomplete">OnGetPinStateComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>. 


Invoking this method requires administrator privileges.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>