---
UID: NN:uiautomationclient.IUIAutomation5
title: IUIAutomation5 (uiautomationclient.h)
description: Extends the IUIAutomation4 interface to expose additional methods for controlling Microsoft UI Automation functionality.helpviewer_keywords: ["IUIAutomation5","IUIAutomation5 interface [Windows Accessibility]","IUIAutomation5 interface [Windows Accessibility]","described","uiautomationclient/IUIAutomation5","winauto.uiauto_IUIAutomation5"]
old-location: winauto\uiauto_IUIAutomation5.htm
tech.root: WinAuto
ms.assetid: BCF67DB0-DF5B-4CED-9C32-01F126494129
ms.date: 12/05/2018
ms.keywords: IUIAutomation5, IUIAutomation5 interface [Windows Accessibility], IUIAutomation5 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation5, winauto.uiauto_IUIAutomation5
f1_keywords:
- uiautomationclient/IUIAutomation5
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
- IUIAutomation5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation5 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation4">IUIAutomation4</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation5</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation4">IUIAutomation4</a>. <b>IUIAutomation5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomation5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler">AddNotificationEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles notification events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler">RemoveNotificationEventHandler</a>
</td>
<td align="left" width="63%">
Removes a notification event handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation4">IUIAutomation4</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
 

 

