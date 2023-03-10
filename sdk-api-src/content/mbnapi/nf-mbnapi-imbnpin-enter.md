---
UID: NF:mbnapi.IMbnPin.Enter
title: IMbnPin::Enter (mbnapi.h)
description: Enters a PIN.
helpviewer_keywords: ["Enter","Enter method [Microsoft Broadband Networks]","Enter method [Microsoft Broadband Networks]","IMbnPin interface","IMbnPin interface [Microsoft Broadband Networks]","Enter method","IMbnPin.Enter","IMbnPin::Enter","mbn.imbnpin_enter","mbnapi/IMbnPin::Enter"]
old-location: mbn\imbnpin_enter.htm
tech.root: mbn
ms.assetid: 71bc0da9-af41-42d6-a7dc-91be54eb6f5c
ms.date: 12/05/2018
ms.keywords: Enter, Enter method [Microsoft Broadband Networks], Enter method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],Enter method, IMbnPin.Enter, IMbnPin::Enter, mbn.imbnpin_enter, mbnapi/IMbnPin::Enter
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
 - IMbnPin::Enter
 - mbnapi/IMbnPin::Enter
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
 - IMbnPin.Enter
---

# IMbnPin::Enter


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Enters a PIN.

## -parameters

### -param pin [in]

The PIN value for the PIN type.

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

The <b>Enter</b> method enters the PIN for the PIN type. The  <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pintype">PinType</a> property of this <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> represents the type of PIN that is to be entered. <i>pin</i> contains the PIN to be entered for the PIN type.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-onentercomplete">OnEnterComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>