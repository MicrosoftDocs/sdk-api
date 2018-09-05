---
UID: NF:mbnapi.IMbnPin.Enter
title: IMbnPin::Enter
author: windows-sdk-content
description: Enters a PIN.
old-location: mbn\imbnpin_enter.htm
old-project: mbn
ms.assetid: 71bc0da9-af41-42d6-a7dc-91be54eb6f5c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enter, Enter method [Microsoft Broadband Networks], Enter method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],Enter method, IMbnPin.Enter, IMbnPin::Enter, mbn.imbnpin_enter, mbnapi/IMbnPin::Enter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPin.Enter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnPin::Enter


## -description


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



The <b>Enter</b> method enters the PIN for the PIN type. The  <a href="https://msdn.microsoft.com/b80d552f-1900-4590-baa5-2fcdb9b32950">PinType</a> property of this <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> represents the type of PIN that is to be entered. <i>pin</i> contains the PIN to be entered for the PIN type.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/6a4bc731-e498-4afb-a648-0b49d2f592ca">OnEnterComplete</a> method of  <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a>
 

 

