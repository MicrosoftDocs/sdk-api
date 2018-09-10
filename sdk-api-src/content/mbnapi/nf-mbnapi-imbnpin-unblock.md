---
UID: NF:mbnapi.IMbnPin.Unblock
title: IMbnPin::Unblock
author: windows-sdk-content
description: Unblocks a blocked PIN.
old-location: mbn\imbnpin_unblock.htm
tech.root: mbn
ms.assetid: 7e5ec24c-681c-4259-9f6a-949bf40d5b3e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnPin interface [Microsoft Broadband Networks],Unblock method, IMbnPin.Unblock, IMbnPin::Unblock, Unblock, Unblock method [Microsoft Broadband Networks], Unblock method [Microsoft Broadband Networks],IMbnPin interface, mbn.imbnpin_unblock, mbnapi/IMbnPin::Unblock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMbnPin.Unblock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnPin::Unblock


## -description


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



The <b>Unblock</b> method unblocks the PIN for the pin type by entering the PUK and sets a new PIN. The <a href="https://msdn.microsoft.com/b80d552f-1900-4590-baa5-2fcdb9b32950">PinType</a> property of this <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> represents the type of PIN which is being changed.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/65a18fee-6d20-42fc-b1cb-ed0a440d76a5">OnUnblockComplete</a> method of  <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a>.

Whenever the <a href="https://msdn.microsoft.com/34378403-cf58-4ada-9eb6-f5dad5f69bc9">GetPinState</a> method of <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> results with the current PIN state set to <b>MBN_PIN_STATE_UNBLOCK</b>, then the application should use <b>Unblock</b> on the PIN type which is returned in <b>PinInfo.pinType</b> passed by the <a href="https://msdn.microsoft.com/e228073b-896a-4d2d-a8a5-f8fa7a52ffc2">OnGetPinStateComplete</a> method of  <a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>. 


Invoking this method requires administrator privileges.




## -see-also




<a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a>
 

 

