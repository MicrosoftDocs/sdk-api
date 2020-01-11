---
UID: NF:mbnapi.IMbnPin.Change
title: IMbnPin::Change (mbnapi.h)
description: Changes the PIN.
old-location: mbn\imbnpin_change.htm
tech.root: mbn
ms.assetid: cf4fac68-65c8-456e-8381-e3f582fc836c
ms.date: 12/05/2018
ms.keywords: Change, Change method [Microsoft Broadband Networks], Change method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],Change method, IMbnPin.Change, IMbnPin::Change, mbn.imbnpin_change, mbnapi/IMbnPin::Change
f1_keywords:
- mbnapi/IMbnPin.Change
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnPin.Change
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnPin::Change


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Changes the PIN.


## -parameters




### -param pin [in]

The current PIN for this PIN type.


### -param newPin [in]

The new PIN for this PIN type.


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



The <b>Change</b> method changes the PIN for the PIN type. The <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pintype">PinType</a> property of this <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> represents the type of PIN to be changed.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-onchangecomplete">OnChangeComplete</a> method of  <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>


.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>
 

 

