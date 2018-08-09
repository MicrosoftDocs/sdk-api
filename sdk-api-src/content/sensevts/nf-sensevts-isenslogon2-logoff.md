---
UID: NF:sensevts.ISensLogon2.Logoff
title: ISensLogon2::Logoff
author: windows-sdk-content
description: The Logoff method notifies an application that a user is logged off.
old-location: sens\isenslogon2_logoff.htm
old-project: sens
ms.assetid: a366a9ca-ce3a-4800-90c6-e1ba53e4cb30
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISensLogon2 interface [SENS],Logoff method, ISensLogon2.Logoff, ISensLogon2::Logoff, Logoff, Logoff method [SENS], Logoff method [SENS],ISensLogon2 interface, _zaw_isenslogon2_logoff, sens.isenslogon2_logoff, sensevts/ISensLogon2::Logoff, syncmgr.isenslogon2_logoff
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
 - ISensLogon2.Logoff
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: ADAM
---

# ISensLogon2::Logoff


## -description


The 
<b>Logoff</b> method notifies an application that a user is logged off.


## -parameters




### -param bstrUserName [in]

The name of a user who logs off.


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



SENS calls this method to notify an application that a user is logged off.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/be61b5b9-d4f1-40ea-a734-7b02c06e41e8">ISensLogon2</a>



<a href="https://msdn.microsoft.com/b45658a1-d427-42b2-912c-5e5c36dab280">ISensLogon::Logoff</a>



<a href="https://msdn.microsoft.com/90c40b7a-e324-43fc-a1e6-f29997ed9436">Terminal Services</a>
 

 

