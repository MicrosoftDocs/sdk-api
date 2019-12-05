---
UID: NN:sensevts.ISensNetwork
title: ISensNetwork (sensevts.h)
description: The ISensNetwork interface handles network events fired by the System Event Notification Service (SENS).
old-location: sens\isensnetwork.htm
tech.root: Sens
ms.assetid: 1cea5dff-13ea-4afb-84ac-7b8df4f55fc8
ms.date: 12/05/2018
ms.keywords: ISensNetwork, ISensNetwork interface [SENS], ISensNetwork interface [SENS],described, _zaw_isensnetwork, sens.isensnetwork, sensevts/ISensNetwork, syncmgr.isensnetwork
ms.topic: interface
f1_keywords:
- sensevts/ISensNetwork
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
- ISensNetwork
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensNetwork interface


## -description


The 
<b>ISensNetwork</b> interface handles network events fired by the System Event Notification Service (SENS).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISensNetwork</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISensNetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISensNetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionlost">ConnectionLost</a>
</td>
<td align="left" width="63%">
Specified connection has been dropped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmade">ConnectionMade</a>
</td>
<td align="left" width="63%">
Specified connection has been established.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmadenoqocinfo">ConnectionMadeNoQOCInfo</a>
</td>
<td align="left" width="63%">
Specified connection has been established with no Quality of Connection information available.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isensonnow">ISensOnNow</a>
 

 

