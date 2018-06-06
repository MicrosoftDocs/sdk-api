---
UID: NF:sensevts.ISensLogon2.Logon
title: ISensLogon2::Logon
author: windows-sdk-content
description: The Logon method notifies an application that a user is logged on.
old-location: sens\isenslogon2_logon.htm
old-project: Sens
ms.assetid: 36caaccf-0cb3-47b8-b0bc-68f9bb21f235
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISensLogon2 interface [SENS],Logon method, ISensLogon2.Logon, ISensLogon2::Logon, Logon, Logon method [SENS], Logon method [SENS],ISensLogon2 interface, _zaw_isenslogon2_logon, sens.isenslogon2_logon, sensevts/ISensLogon2::Logon, syncmgr.isenslogon2_logon
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
 - ISensLogon2.Logon
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISensLogon2::Logon


## -description


The 
<b>Logon</b> method notifies an application that a user is logged on.


## -parameters




### -param bstrUserName [in]

The name of a user who is logged on.


### -param dwSessionId [in]

The session identifier of a session.


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



SENS calls this method to notify an application that a user is logged on.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/be61b5b9-d4f1-40ea-a734-7b02c06e41e8">ISensLogon2</a>



<a href="https://msdn.microsoft.com/76a811a2-70c4-4dda-99c0-1578e9402a3b">ISensLogon::Logon</a>



<a href="https://msdn.microsoft.com/90c40b7a-e324-43fc-a1e6-f29997ed9436">Terminal Services</a>
 

 

