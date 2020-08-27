---
UID: NN:sensevts.ISensLogon2
title: ISensLogon2 (sensevts.h)
description: The ISensLogon2 interface handles logon events fired by SENS.
helpviewer_keywords: ["ISensLogon2","ISensLogon2 interface [SENS]","ISensLogon2 interface [SENS]","described","_zaw_isenslogon2","sens.isenslogon2","sensevts/ISensLogon2","syncmgr.isenslogon2"]
old-location: sens\isenslogon2.htm
tech.root: Sens
ms.assetid: be61b5b9-d4f1-40ea-a734-7b02c06e41e8
ms.date: 12/05/2018
ms.keywords: ISensLogon2, ISensLogon2 interface [SENS], ISensLogon2 interface [SENS],described, _zaw_isenslogon2, sens.isenslogon2, sensevts/ISensLogon2, syncmgr.isenslogon2
f1_keywords:
- sensevts/ISensLogon2
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
- ISensLogon2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensLogon2 interface


## -description


The 
<b>ISensLogon2</b> interface handles logon events fired by SENS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensLogon2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISensLogon2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon2-logoff">Logoff</a>
</td>
<td align="left" width="63%">
A user has logged off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon2-logon">Logon</a>
</td>
<td align="left" width="63%">
A user has logged on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon2-postshell">PostShell</a>
</td>
<td align="left" width="63%">
A user has logged on and Windows Explorer (Shell) is up and running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon2-sessiondisconnect">SessionDisconnect</a>
</td>
<td align="left" width="63%">
A session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon2-sessionreconnect">SessionReconnect</a>
</td>
<td align="left" width="63%">
A session has been reconnected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>
 

 

