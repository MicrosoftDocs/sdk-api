---
UID: NN:uiautomationclient.IUIAutomation4
title: IUIAutomation4
author: windows-sdk-content
description: Extends the IUIAutomation3 interface to expose additional methods for controlling Microsoft UI Automation functionality.
old-location: winauto\uiauto_IUIAutomation4.htm
old-project: WinAuto
ms.assetid: CA616076-CD04-4753-9605-093C9529C826
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomation4, IUIAutomation4 interface [Windows Accessibility], IUIAutomation4 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation4, winauto.uiauto_IUIAutomation4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomation4
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation4 interface


## -description


Extends the <a href="https://msdn.microsoft.com/D46CE3FF-31E2-32CE-FD38-680064E1765D">IUIAutomation3</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation4</b> interface inherits from <a href="https://msdn.microsoft.com/D46CE3FF-31E2-32CE-FD38-680064E1765D">IUIAutomation3</a>. <b>IUIAutomation4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E479ACCA-9372-463F-A992-8030E33A2341">AddChangesEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles change events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18F65528-3038-4FF7-AEB8-AAEA3A5BB058">RemoveChangesEventHandler</a>
</td>
<td align="left" width="63%">
Removes a changes event handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D46CE3FF-31E2-32CE-FD38-680064E1765D">IUIAutomation3</a>



<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

