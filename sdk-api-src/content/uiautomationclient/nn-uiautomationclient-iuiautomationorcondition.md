---
UID: NN:uiautomationclient.IUIAutomationOrCondition
title: IUIAutomationOrCondition
author: windows-sdk-content
description: Represents a condition made up of multiple conditions, at least one of which must be true.
old-location: winauto\uiauto_IUIAutomationOrCondition.htm
tech.root: WinAuto
ms.assetid: 323dedd5-2799-4fcc-bc8c-56b39ab7f882
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomationOrCondition, IUIAutomationOrCondition interface [Windows Accessibility], IUIAutomationOrCondition interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationOrCondition, uiauto_IUIAutomationOrCondition, uiautomationclient/IUIAutomationOrCondition, winauto.uiauto_IUIAutomationOrCondition
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
 - IUIAutomationOrCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationOrCondition interface


## -description


Represents a condition made up of multiple conditions, at least one of which must be true.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationOrCondition</b> interface inherits from <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>. <b>IUIAutomationOrCondition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationOrCondition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1af107d-2916-4061-9515-002c3af6eb00">GetChildren</a>
</td>
<td align="left" width="63%">
Retrieves the conditions that make up this condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8c45ccb-5e3c-4816-8ffe-6865a7794e8b">GetChildrenAsNativeArray</a>
</td>
<td align="left" width="63%">
Retrieves the conditions that make up this condition, as an ordinary array.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationOrCondition</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2dce4d7d-73c4-4882-953e-c7bbf1c1c0e7">ChildCount</a>


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
 

 

