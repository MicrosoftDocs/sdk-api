---
UID: NN:sensevts.ISensLogon
title: ISensLogon
author: windows-sdk-content
description: The ISensLogon interface handles logon events fired by SENS.
old-location: sens\isenslogon.htm
tech.root: Sens
ms.assetid: 77c02510-6386-4f6d-af1a-e7337f5d347d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISensLogon, ISensLogon interface [SENS], ISensLogon interface [SENS],described, _zaw_isenslogon, sens.isenslogon, sensevts/ISensLogon, syncmgr.isenslogon
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
 - ISensLogon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensLogon interface


## -description


The 
<b>ISensLogon</b> interface handles logon events fired by SENS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensLogon</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISensLogon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISensLogon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1675ffc7-7031-492d-bf39-64281a16a074">DisplayLock</a>
</td>
<td align="left" width="63%">
Screen display has been locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1b1beb-f59a-4990-84e1-deca1432f6cf">DisplayUnlock</a>
</td>
<td align="left" width="63%">
Screen display has been unlocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b45658a1-d427-42b2-912c-5e5c36dab280">Logoff</a>
</td>
<td align="left" width="63%">
A user has logged off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a811a2-70c4-4dda-99c0-1578e9402a3b">Logon</a>
</td>
<td align="left" width="63%">
A user has logged on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47531e1f-e2d4-4475-a109-e213c903a7ba">StartScreenSaver</a>
</td>
<td align="left" width="63%">
Screen saver has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bde3bda-c0ed-4303-b6c1-dd667e9b7504">StartShell</a>
</td>
<td align="left" width="63%">
Shell has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61a6434b-1a80-4a37-9175-636c3792a865">StopScreenSaver</a>
</td>
<td align="left" width="63%">
Screen saver has been stopped.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/1cea5dff-13ea-4afb-84ac-7b8df4f55fc8">ISensNetwork</a>



<a href="https://msdn.microsoft.com/39d483be-8dbd-41f9-9804-af9dc4535c05">ISensOnNow</a>
 

 

