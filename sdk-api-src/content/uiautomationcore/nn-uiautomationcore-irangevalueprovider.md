---
UID: NN:uiautomationcore.IRangeValueProvider
title: IRangeValueProvider
author: windows-sdk-content
description: Provides access to controls that can be set to a value within a range.
old-location: winauto\uiauto_IRangeValueProvider.htm
old-project: WinAuto
ms.assetid: 1e9e39f9-e728-4ed6-bc62-80d3bbe6302d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IRangeValueProvider, IRangeValueProvider interface [Windows Accessibility], IRangeValueProvider interface [Windows Accessibility],described, uiauto.uiauto_IRangeValueProvider, uiauto_IRangeValueProvider, uiautomationcore/IRangeValueProvider, winauto.uiauto_IRangeValueProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - IRangeValueProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRangeValueProvider interface


## -description


Provides access to controls that can be set to a value within a range.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeValueProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRangeValueProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRangeValueProvider</b> interface has these methods.
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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeValueProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5edb8de2-3c42-4df4-b6f8-5dd0e812d749">IsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the value of a control is read-only. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5f6d5a05-f91d-48ee-8782-f39661051584">LargeChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">

        Specifies the value that is added to or subtracted from the <a href="https://msdn.microsoft.com/b17ca8c8-948b-4d92-a6c7-79e610aa8e4a">IRangeValueProvider::Value</a> 
        property when a large change is made, such as when the PAGE DOWN key is pressed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a681b992-c3db-497a-ae38-df62f9016ba6">Maximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the maximum range value supported by the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6704d5d8-7024-4010-a212-2ffccfae0cbf">Minimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the minimum range value supported by the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8230747d-d8c3-4708-a77a-7c76a62f39dd">SmallChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">

        Specifies the value that is added to or subtracted from the <a href="https://msdn.microsoft.com/b17ca8c8-948b-4d92-a6c7-79e610aa8e4a">IRangeValueProvider::Value</a> property 
        when a small change is made, such as when an arrow key is pressed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the value of the control.

</td>
</tr>
</table> 


## -remarks




            Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546453">RangeValue</a> control pattern.
            




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

