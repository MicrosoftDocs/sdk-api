---
UID: NF:sensevts.ISensLogon2.PostShell
title: ISensLogon2::PostShell
author: windows-sdk-content
description: Use the PostShell method when a user has logged on and Windows Explorer is running. This method is different from the Logon method because Logon is called after logon when the Shell may not yet be running.
old-location: sens\isenslogon2_sessionpostshell.htm
old-project: Sens
ms.assetid: fa187b3c-fc78-410f-9339-9b4c94c43f95
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISensLogon2 interface [SENS],PostShell method, ISensLogon2.PostShell, ISensLogon2::PostShell, PostShell, PostShell method [SENS], PostShell method [SENS],ISensLogon2 interface, _zaw_isenslogon2_sessionpostshell, sens.isenslogon2_sessionpostshell, sensevts/ISensLogon2::PostShell, syncmgr.isenslogon2_sessionpostshell
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
 - ISensLogon2.PostShell
 - ISensLogon2.PostShell
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: ADAM
---

# ISensLogon2::PostShell


## -description


Use the 
<b>PostShell</b> method when a user has logged on and Windows Explorer is running. This method is different from the 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt187885">Logon</a> method because 
<b>Logon</b> is called after logon when the Shell may not yet be running.


## -parameters




### -param bstrUserName [in]

Name of the current user.


### -param dwSessionId [in]

The session identifier of the session.


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
Method returned successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify your application that a user has logged on and the Windows Explorer (Shell) is running.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/be61b5b9-d4f1-40ea-a734-7b02c06e41e8">ISensLogon2</a>



<a href="https://msdn.microsoft.com/b45658a1-d427-42b2-912c-5e5c36dab280">ISensLogon::Logoff</a>



<a href="https://msdn.microsoft.com/90c40b7a-e324-43fc-a1e6-f29997ed9436">Terminal Services</a>
 

 

