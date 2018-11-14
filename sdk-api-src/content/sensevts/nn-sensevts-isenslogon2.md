---
UID: NN:sensevts.ISensLogon2
title: ISensLogon2
author: windows-sdk-content
description: The ISensLogon2 interface handles logon events fired by SENS.
old-location: sens\isenslogon2.htm
tech.root: Sens
ms.assetid: be61b5b9-d4f1-40ea-a734-7b02c06e41e8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISensLogon2, ISensLogon2 interface [SENS], ISensLogon2 interface [SENS],described, _zaw_isenslogon2, sens.isenslogon2, sensevts/ISensLogon2, syncmgr.isenslogon2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: 
req.dll: Sens.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensLogon2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensLogon2 interface


## -description


The 
<b>ISensLogon2</b> interface handles logon events fired by SENS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensLogon2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISensLogon2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISensLogon2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a366a9ca-ce3a-4800-90c6-e1ba53e4cb30">Logoff</a>
</td>
<td align="left" width="63%">
A user has logged off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36caaccf-0cb3-47b8-b0bc-68f9bb21f235">Logon</a>
</td>
<td align="left" width="63%">
A user has logged on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa187b3c-fc78-410f-9339-9b4c94c43f95">PostShell</a>
</td>
<td align="left" width="63%">
A user has logged on and Windows Explorer (Shell) is up and running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afa56cb1-7c52-48db-ac7c-237cb49cc97f">SessionDisconnect</a>
</td>
<td align="left" width="63%">
A session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b789a75d-e842-40b4-9e8d-b9374b5ba6b0">SessionReconnect</a>
</td>
<td align="left" width="63%">
A session has been reconnected.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>
 

 

