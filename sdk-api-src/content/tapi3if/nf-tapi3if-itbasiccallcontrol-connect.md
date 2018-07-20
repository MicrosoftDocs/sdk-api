---
UID: NF:tapi3if.ITBasicCallControl.Connect
title: ITBasicCallControl::Connect
author: windows-sdk-content
description: The Connect method attempts to complete the connection of an outgoing call.
old-location: tapi3\itbasiccallcontrol_connect.htm
old-project: tapi
ms.assetid: cc9a8bfd-14c0-459c-a911-325b73323c08
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: Connect, Connect method [TAPI 2.2], Connect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Connect method, ITBasicCallControl.Connect, ITBasicCallControl::Connect, _tapi3_itbasiccallcontrol_connect, tapi3.itbasiccallcontrol_connect, tapi3if/ITBasicCallControl::Connect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.Connect
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl::Connect


## -description


The 
<b>Connect</b> method attempts to complete the connection of an outgoing call.


## -parameters




### -param fSync [in]

Boolean indicating whether connection is to be performed synchronously (VARIANT_TRUE) or asynchronously (VARIANT_FALSE).


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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">Call state</a> must be CS_IDLE.

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
</table>
 




## -remarks



If the call is asynchronous, the application will receive information about the call's progress through the 
<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a> outgoing interface. The application must register the outgoing interface before calling 
<b>Connect</b>. 
<b>Connect</b> may return S_OK, but the actual connection may fail (and the application will be notified through the outgoing interface).

If the call is synchronous, this method will not return until the call is in the connected state or fails.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/71e61376-7913-42a9-a8e2-2ea6e4918f30">Complete a Session</a>



<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>
 

 

