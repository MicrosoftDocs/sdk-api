---
UID: NN:sensevts.ISensLogon
title: ISensLogon (sensevts.h)
description: The ISensLogon interface handles logon events fired by SENS.helpviewer_keywords: ["ISensLogon","ISensLogon interface [SENS]","ISensLogon interface [SENS]","described","_zaw_isenslogon","sens.isenslogon","sensevts/ISensLogon","syncmgr.isenslogon"]
old-location: sens\isenslogon.htm
tech.root: Sens
ms.assetid: 77c02510-6386-4f6d-af1a-e7337f5d347d
ms.date: 12/05/2018
ms.keywords: ISensLogon, ISensLogon interface [SENS], ISensLogon interface [SENS],described, _zaw_isenslogon, sens.isenslogon, sensevts/ISensLogon, syncmgr.isenslogon
f1_keywords:
- sensevts/ISensLogon
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensLogon interface


## -description


The 
<b>ISensLogon</b> interface handles logon events fired by SENS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensLogon</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISensLogon</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displaylock">DisplayLock</a>
</td>
<td align="left" width="63%">
Screen display has been locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displayunlock">DisplayUnlock</a>
</td>
<td align="left" width="63%">
Screen display has been unlocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logoff">Logoff</a>
</td>
<td align="left" width="63%">
A user has logged off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logon">Logon</a>
</td>
<td align="left" width="63%">
A user has logged on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-startscreensaver">StartScreenSaver</a>
</td>
<td align="left" width="63%">
Screen saver has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-startshell">StartShell</a>
</td>
<td align="left" width="63%">
Shell has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-stopscreensaver">StopScreenSaver</a>
</td>
<td align="left" width="63%">
Screen saver has been stopped.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isensnetwork">ISensNetwork</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isensonnow">ISensOnNow</a>
 

 

