---
UID: NN:uiautomationclient.IUIAutomationRangeValuePattern
title: IUIAutomationRangeValuePattern
author: windows-sdk-content
description: Provides access to a control that presents a range of values.
old-location: winauto\uiauto_IUIAutomationRangeValuePattern.htm
old-project: WinAuto
ms.assetid: 145c14e5-1b6b-4eb1-a73a-aa59b5e1b4c4
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationRangeValuePattern, IUIAutomationRangeValuePattern interface [Windows Accessibility], IUIAutomationRangeValuePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationRangeValuePattern, uiauto_IUIAutomationRangeValuePattern, uiautomationclient/IUIAutomationRangeValuePattern, winauto.uiauto_IUIAutomationRangeValuePattern
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationRangeValuePattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationRangeValuePattern interface


## -description


Provides access to a control that presents a range of values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationRangeValuePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationRangeValuePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationRangeValuePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationRangeValuePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93e8df1a-8e07-4efa-8f0e-81aa7f4a3171">CachedIsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the value of the element can be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d97addfd-53ae-4445-9f77-d24d97644bfc">CachedLargeChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e5bae825-8e42-4ecb-b891-b802ca8d3360">CachedMaximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached maximum value of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40fe6309-8648-49b2-990c-78e7a65ef5ed">CachedMinimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached minimum value of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d737eaa-eb4a-4d73-b515-876961423fd6">CachedSmallChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2a5ca86d-75d1-416e-9801-52d855c90c08">CachedValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached value of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0c3561b0-3739-463c-8856-84d1ab565506">CurrentIsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the value of the element can be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/801d7a2c-387f-4770-980a-fc5fb98959d8">CurrentLargeChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3053b901-ec5d-4bfa-ab2f-1ea6b9517f13">CurrentMaximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the maximum value of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1bb98417-750c-4b03-a4a2-d652d0c2fb6e">CurrentMinimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum value of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/88de76d5-100c-41b9-b87e-2d1c3bf6e633">CurrentSmallChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0602822f-750e-49a3-afb4-cf5ce777ea61">CurrentValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the value of the control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

