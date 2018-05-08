---
UID: NF:mbnapi.IMbnPin.Enable
title: IMbnPin::Enable
author: windows-driver-content
description: Enables a PIN.
old-location: mbn\imbnpin_enable.htm
old-project: mbn
ms.assetid: bbdd767b-f08a-4e94-bccf-9ed0d1b4af29
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Enable, Enable method [Microsoft Broadband Networks], Enable method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],Enable method, IMbnPin.Enable, IMbnPin::Enable, mbn.imbnpin_enable, mbnapi/IMbnPin::Enable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnPin.Enable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnPin::Enable


## -description


Enables a PIN.


## -parameters




### -param pin [in]

The PIN value for the PIN type to be enabled.


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



The <b>Enable</b> method enables the PIN type for the Mobile Broadband device. The <a href="https://msdn.microsoft.com/b80d552f-1900-4590-baa5-2fcdb9b32950">PinType</a> property of <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> represents the type of PIN to be activated. <i>pin</i> contains the current value of the PIN for the PIN type.

This is an asynchronous operation. If the method returns with success, then upon completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/577ba161-dbde-4541-8098-72ab682e548b">OnEnableComplete</a> method of  <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a>
 

 

