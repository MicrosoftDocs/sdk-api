---
UID: NN:uiautomationclient.IUIAutomation3
title: IUIAutomation3 (uiautomationclient.h)
description: Extends the IUIAutomation2 interface to expose additional methods for controlling Microsoft UI Automation functionality.
helpviewer_keywords: ["IUIAutomation3","IUIAutomation3 interface [Windows Accessibility]","IUIAutomation3 interface [Windows Accessibility]","described","uiautomationclient/IUIAutomation3","winauto.uiauto_IUIAutomation3"]
old-location: winauto\uiauto_IUIAutomation3.htm
tech.root: WinAuto
ms.assetid: D46CE3FF-31E2-32CE-FD38-680064E1765D
ms.date: 12/05/2018
ms.keywords: IUIAutomation3, IUIAutomation3 interface [Windows Accessibility], IUIAutomation3 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation3, winauto.uiauto_IUIAutomation3
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation3
 - uiautomationclient/IUIAutomation3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomation3
---

# IUIAutomation3 interface


## -description

Extends the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation3</b> interface inherits from <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a>. <b>IUIAutomation3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomation3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation3-addtextedittextchangedeventhandler">AddTextEditTextChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles programmatic text-edit events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation3-removetextedittextchangedeventhandler">RemoveTextEditTextChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a programmatic text-edit event handler.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a>



<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>