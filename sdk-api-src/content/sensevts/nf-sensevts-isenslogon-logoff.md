---
UID: NF:sensevts.ISensLogon.Logoff
title: ISensLogon::Logoff
author: windows-sdk-content
description: The Logoff method notifies an application that a user is logged off.
old-location: sens\isenslogon_logoff.htm
old-project: Sens
ms.assetid: b45658a1-d427-42b2-912c-5e5c36dab280
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISensLogon interface [SENS],Logoff method, ISensLogon.Logoff, ISensLogon::Logoff, Logoff, Logoff method [SENS], Logoff method [SENS],ISensLogon interface, _zaw_isenslogon_logoff, sens.isenslogon_logoff, sensevts/ISensLogon::Logoff, syncmgr.isenslogon_logoff
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensevts.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
tech.root: 
req.typenames: QOCINFO, *LPQOCINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensLogon.Logoff
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: ADAM
---

# ISensLogon::Logoff


## -description


The 
<b>Logoff</b> method notifies an application that a user is logged off.


## -parameters




### -param bstrUserName [in]

The name of a user who logs off.


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
The method returns successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify an application that a user is logged off.

<div class="alert"><b>Important</b>  This function will not work with multiple logins through Remote Desktop Services and does not support Remote Desktop Services or Fast-User Switching scenarios. Desktop applications can register for session changes notifications by calling <a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a>. Services can handle session change notifications via SERVICE_CONTROL_SESSIONCHANGE control codes in their <a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> callback function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/library/ms686510(v=VS.85).aspx">IEventSubscription</a>



<a href="https://msdn.microsoft.com/library/ms685465(v=VS.85).aspx">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/77c02510-6386-4f6d-af1a-e7337f5d347d">ISensLogon</a>



<a href="https://msdn.microsoft.com/76a811a2-70c4-4dda-99c0-1578e9402a3b">ISensLogon::Logon</a>
 

 

