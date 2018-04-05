---
UID: NN:uiautomationclient.IUIAutomationAndCondition
title: IUIAutomationAndCondition
author: windows-driver-content
description: Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.
old-location: winauto\uiauto_IUIAutomationAndCondition.htm
old-project: WinAuto
ms.assetid: f9808c48-dc98-465b-958d-223a8b7cc371
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IUIAutomationAndCondition, IUIAutomationAndCondition interface [Windows Accessibility], IUIAutomationAndCondition interface [Windows Accessibility], described, uiauto.uiauto_IUIAutomationAndCondition, uiauto_IUIAutomationAndCondition, uiautomationclient/IUIAutomationAndCondition, winauto.uiauto_IUIAutomationAndCondition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationAndCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationAndCondition interface


## -description


Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationAndCondition</b> interface inherits from <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>. <b>IUIAutomationAndCondition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationAndCondition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6868fae6-74fb-4133-8dc5-73ce5f8a6f7b">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves the conditions that make up this condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2543dd60-88cb-4477-9008-4ec8f9d8f287">GetChildrenAsNativeArray</a>
</td>
<td align="left" width="63%">
Retrieves the conditions that make up this condition, as an ordinary array.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationAndCondition</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9e87bc65-5b41-4256-92c7-21b92032b83f">ChildCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of conditions that make up this condition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>



<a href="https://msdn.microsoft.com/cea34e47-03a9-4ff9-9019-427a2a3e13d6">Property Condition Interfaces for Clients</a>
 

 

