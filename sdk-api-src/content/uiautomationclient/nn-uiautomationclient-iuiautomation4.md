---
UID: NN:uiautomationclient.IUIAutomation4
title: IUIAutomation4 (uiautomationclient.h)
description: Extends the IUIAutomation3 interface to expose additional methods for controlling Microsoft UI Automation functionality.
old-location: winauto\uiauto_IUIAutomation4.htm
tech.root: WinAuto
ms.assetid: CA616076-CD04-4753-9605-093C9529C826
ms.date: 12/05/2018
ms.keywords: IUIAutomation4, IUIAutomation4 interface [Windows Accessibility], IUIAutomation4 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation4, winauto.uiauto_IUIAutomation4
f1_keywords:
- uiautomationclient/IUIAutomation4
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IUIAutomation4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation4 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation3">IUIAutomation3</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation3">IUIAutomation3</a>. <b>IUIAutomation4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomation4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-addchangeseventhandler">AddChangesEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles change events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-removechangeseventhandler">RemoveChangesEventHandler</a>
</td>
<td align="left" width="63%">
Removes a changes event handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation3">IUIAutomation3</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
 

 

